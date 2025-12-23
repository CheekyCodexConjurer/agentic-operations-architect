# Merge Protocol (Idempotent)

This protocol ensures repeated runs do not rewrite or destroy existing content.

## Rules
1. Never delete or rename existing agent files by default.
2. If a file must be updated, write within explicit markers.
3. If conflicts exist, add a note under `.agent-docs/compat/`.
4. Re-running the same operation must not duplicate content.

## Marker Format
Use a consistent block marker when modifying an existing file:

```
<!-- AOA:BEGIN -->
... inserted content ...
<!-- AOA:END -->
```

If the block exists, update the content inside the markers only.
