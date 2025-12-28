# Agent Management Guide

This guide defines auto-managed agent lifecycle and coverage.

## Files
- `.agent-docs/memory/AGENTS_REGISTRY.md`
- `.agent-docs/memory/AGENTS_REGISTRY.json`
- `.agent-docs/memory/AGENT_PROPOSALS.md`
- `.agent-docs/agents/AGENT_TEMPLATE.md`

## Lifecycle States
- proposed: awaiting approval
- active: in use and current
- needs_update: drift detected
- stale: inactive or low usage
- retire_candidate: safe to remove after review
- retired: kept for history only

## Workflow
1. Run `agent_manager` at session start and after major structural changes.
2. Register every `AGENTS.md` and `AGENTS.override.md` with scope and owner.
3. Compare coverage with repo index and architecture maps.
4. Propose new agents for uncovered domains with objective and scope.
5. Detect drift by comparing scope file timestamps to agent instructions.
6. Mark updates or retirement candidates in the registry.
7. When proposals are approved, scaffold new `AGENTS.md` from the template.
8. Use the agent management checklist for completeness.

## Fixed Agents
- Mark fixed agents as `fixed: true` in the registry.
- Do not edit fixed agents; only propose updates.
- Keep a short rationale in the registry notes.

## Placement
- Use scoped `AGENTS.md` in the directories they should govern.
- Keep the root `AGENTS.md` minimal and link to this guide.

## Approval Loop
- Proposals live in `AGENT_PROPOSALS.md`.
- Explain each proposal objective before asking for approval.
- Approve by setting `status` to `approved`.
- Once approved, scaffold and activate the agent.
