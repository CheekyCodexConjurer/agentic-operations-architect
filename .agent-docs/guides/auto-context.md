# Auto-Context Guide

Auto-context is a temporary, task-scoped memory file used for long runs. It
helps the agent recover context after chat resets or long mapping sessions.

## File Location
- Active file: `.agent-docs/auto-context/AUTO_CONTEXT.md`
- Archive files: `.agent-docs/auto-context/AUTO_CONTEXT_<timestamp>_<slug>.md`

## When to Update
- After meaningful milestones.
- After a large mapping batch.
- Before changing strategy or scope.

## Rotation Policy (Per Task)
- When a task is complete, rename the active file to the archive format.
- Start a new `AUTO_CONTEXT.md` for the next task.
- Use a short slug that describes the task (example: `map-backend`).

## Handoff Integration
- Update `.agent-docs/memory/HANDOFF.md` before rotating the task context.
- Use `context_compactor` when the log grows too large.

## Content Rules
- Keep entries short and actionable.
- Link to files or ADRs instead of copying content.
- Never include secrets, tokens, or private data.
- Stay within `LINE_BUDGETS.yaml` limits.
