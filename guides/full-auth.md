# Full Auth Guide

Full Auth is an opt-in execution mode that reduces back-and-forth by allowing
the agent to run end-to-end once explicitly authorized.

## When to Use
- Multi-hour tasks.
- Broad refactors with many steps.
- Migration work that needs continuous iteration.

## Requirements
- The user must explicitly authorize end-to-end execution.
- The agent must still respect `.agentignore` and safety rules.

## Output Contract
- Investigation notes.
- Phased plan.
- Implementation narrative by phase.
- Files changed + verification results.
