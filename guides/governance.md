# Governance Guide

This guide defines safety and quality rules for agent-driven changes.

## Safety
- Back up existing agent documentation before overwriting.
- Avoid destructive actions without explicit approval.
- Keep modifications minimal and reversible.
- Respect `.agentignore` forbidden zones without exception.
- Validate modified paths against safety rules before commit.
- Use Shadow Coder for parallel architecture changes.

## Documentation Hygiene
- Update architecture docs when behavior changes.
- Record decisions in the ADR log.
- Keep auto-context short and task-scoped.

## Verification
- Use test-first development when touching behavior.
- Validate changes with tests or reproducible runs.
- Log gaps and unknowns instead of guessing.
