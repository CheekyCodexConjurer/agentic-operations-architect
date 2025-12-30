---
name: autonomy_kickoff
description: Run the full autonomy bootstrap with minimal questions.
metadata:
  short-description: Autonomy kickoff
---

## Purpose
Complete the first-run setup like an installer, with minimal questions.

## Steps
1. Ask for response style and record it.
2. Run non-destructive bootstrap.
3. Run `analyze_repo_capabilities` and `detect_commands`.
4. Populate `QUALITY_GATES.md` with best-known commands.
5. Run `repo_indexer`, `skills_auditor`, and `skills_sync`.
6. Run `agent_manager` to initialize the agent registry and proposals.
7. Run architecture mapping (index-first, baseline in `overview.md`).
8. Initialize Action Log, Handoff, Backlog, and line budgets.
9. Run `refactor_gate` after mapping.
10. Mark `AUTONOMY_MODE.md` as done.
11. Continue end-to-end unless blocked.
