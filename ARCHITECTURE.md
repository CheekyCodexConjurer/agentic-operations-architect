# Architecture Overview

This repository is a documentation-only system that defines how an autonomous
PhD-level software architect should operate inside any target codebase. It
ships governance rules, mapping protocols, and reusable templates.

## System Goal
Enable safe, auditable, and high-fidelity software changes by enforcing
governance, proof-driven development, and living architecture maps.

## Core Layers
- Safety Layer: forbidden zones, pre-commit validation, and non-destructive
  workflows.
- Trust Layer: test-first changes and auto-debug until proof is obtained.
- Decision Memory: ADRs that justify architectural choices.
- Cartography: living architecture maps and interaction graphs.
- Auto-Context: task-scoped continuity for long runs.

## Key Artifacts
- `AGENTS.md`: constitution and protocols.
- `META_INSTRUCTIONS.md`: agent priorities and philosophy.
- `.agentignore`: forbidden zones the agent must never modify.
- `.agent-docs/architecture.md`: architecture index.
- `.agent-docs/architecture/*.md`: interaction maps, flow maps, component
  profiles.
- `.agent-docs/memory/DECISIONS.md`: ADR log.
- `.agent-docs/auto-context/AUTO_CONTEXT.md`: task-scoped context log.
- `.agent-docs/skills/*.md`: skill playbooks for specialized behaviors.

## Interactions and Flow
1. Bootstrap copies the templates into a target repo.
2. The agent reads `AGENTS.md` and `META_INSTRUCTIONS.md` to set priorities.
3. `analyze_repo_capabilities` scans for existing tooling and patterns.
4. The Cartographer maps entrypoints, components, and flows.
5. The Trust Layer enforces TDD, then uses auto-debug on failures.
6. The Safety Layer validates that no forbidden paths were touched.
7. Decision Memory captures major architectural changes in ADRs.
8. Auto-context maintains state for long runs and rotates per task.

## Safety Layer
- `.agentignore` defines protected files and directories.
- Pre-commit validation checks modifications against forbidden zones.
- Shadow Coder supports parallel architecture changes without breakage.

## Trust Layer
- Tests are required before changes in a target area.
- Failures trigger structured debug and root-cause analysis.
- No new code is accepted without passing tests.

## Decision Memory
- Every architectural change receives an ADR with context, decision, and
  consequences.

## Universal Adaptation
- The agent detects repo signatures to activate relevant skills.
- Changes should use AST-based insertion when possible, not raw text edits.
