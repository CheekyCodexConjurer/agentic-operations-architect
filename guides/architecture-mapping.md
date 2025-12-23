# Architecture Mapping Guide

This guide defines how an agent should map execution flow and file-to-file
interactions in a repository. The output is a clear, auditable map of how the
system works.

## Inputs
- Repository file tree.
- Entrypoints (CLI, web servers, workers, scheduled jobs, tests).
- Configuration files and dependency manifests.

## Outputs
- `.agent-docs/architecture.md` updated.
- `.agent-docs/architecture/interaction-map.md` filled.
- `.agent-docs/architecture/flow-map.md` filled.
- `.agent-docs/architecture/component-profile.md` sections created.
- ADR entries for major architectural choices.

## Protocol
1. Define scope and task goal in auto-context.
2. Inventory entrypoints and list their files.
3. Group files into components or modules.
4. Extract interactions:
   - Track imports, calls, events, and shared data stores.
   - Record origin and target at file or component level.
5. Map critical flows:
   - Pick the highest value user paths.
   - Trace the call chain end to end.
6. Capture side effects and external dependencies.
7. Record confidence levels and unknowns.
8. Iterate until coverage is acceptable.

## Mapping Levels
- L0: system overview and purpose.
- L1: components, boundaries, and ownership.
- L2: critical flows and data movement.

## Automation Heuristics
- Start from entrypoints and follow dependency edges outward.
- Prefer static structure first, then validate with a runtime signal if safe.
- Mark low confidence when the link is inferred or unclear.
- Keep a "Gaps" list to drive future mapping.

## Large Repo Strategy
- Partition by domain or service.
- Map one domain per task and rotate auto-context per task.
- Maintain a global index of mapped and unmapped areas.

## Done Criteria
- All entrypoints are listed with owners or locations.
- Critical flows are mapped and reviewed.
- Interaction map shows cross-component edges.
- Unknowns are explicitly logged.
