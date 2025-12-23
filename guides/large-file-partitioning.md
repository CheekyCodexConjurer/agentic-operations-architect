# Large File Partitioning Guide

Use this guide when files are too large to process in one pass.

## Partition Strategy
- Split by logical sections (modules, classes, functions).
- Use file headers or region markers as boundaries.
- Keep chunk size consistent across the task.

## Summary Rules
- Summaries must include purpose, inputs, outputs, and side effects.
- Reference line numbers or section names when possible.
- Capture unresolved questions in the gaps list.

## Reassembly
- Maintain an index of chunks and their summaries.
- Reconstruct the full flow only after all chunks are processed.
