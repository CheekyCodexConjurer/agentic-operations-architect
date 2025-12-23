# Governance Guide

This guide defines safety and quality rules for agent-driven changes.

## Safety
- Avoid overwriting; if required, back up first.
- Avoid destructive actions without explicit approval.
- Keep modifications minimal and reversible.
- Respect `.agentignore` forbidden zones without exception.
- Validate modified paths against safety rules before commit.
- Use Shadow Coder for parallel architecture changes.
- Use merge protocol when touching existing instructions.
- Run safety validation before commits.

## Documentation Hygiene
- Update architecture docs when behavior changes.
- Record decisions in the ADR log.
- Keep auto-context short and task-scoped.
- Update the Action Log for meaningful changes.
- Record recurring patterns in `PATTERNS.md`.

## Verification
- Use test-first development when touching behavior.
- Validate changes with tests or reproducible runs.
- Log gaps and unknowns instead of guessing.
