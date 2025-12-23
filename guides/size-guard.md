# Size Guard Guide

Size Guard keeps context-heavy files between 300-500 lines.

## File
- `.agent-docs/memory/LINE_BUDGETS.yaml`

## Workflow
1. Run `size_guard` before large updates.
2. Rotate or split files that exceed limits.
3. Update indexes to reference new parts.
4. Record the action in the Action Log.

## Architecture Notes
- Split large `flow-map.md` or `interaction-map.md` by domain.
- Keep `ARCHITECTURE.md` and `.agent-docs/architecture.md` index-only.
