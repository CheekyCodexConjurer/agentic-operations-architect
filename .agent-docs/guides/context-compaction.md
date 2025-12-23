# Context Compaction Guide

Context compaction keeps long-run memory small and recoverable.

## Inputs
- `AUTO_CONTEXT.md`
- `ACTION_LOG.md`
- `BACKLOG.md`

## Outputs
- `HANDOFF.md` updated
- `AUTO_CONTEXT.md` rotated or trimmed

## Workflow
1. Summarize the current state into `HANDOFF.md`.
2. Move completed task notes to an archive file.
3. Update `BACKLOG.md` with open items.
4. Record a compact Action Log entry.
