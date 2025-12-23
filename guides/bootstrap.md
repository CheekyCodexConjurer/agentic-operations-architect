# Bootstrap Guide

Use this guide to prepare any repository for agentic work using the templates
and protocols in this repo.

## Steps
1. Copy `templates/AGENTS.md` into the target repo root as `AGENTS.md`.
2. Copy `templates/META_INSTRUCTIONS.md` into the target repo root.
3. Copy `templates/.agentignore` into the target repo root.
4. Copy `templates/.agentpolicy` into the target repo root.
5. Copy `templates/QUALITY_GATES.md` into the target repo root.
6. Copy `templates/ARCHITECTURE.md` into the target repo root.
7. Copy `templates/PLANS.md` into the target repo root.
8. Copy `templates/.codex/skills/` into the target repo as `.codex/skills/`.
9. Copy `templates/agent-docs/` into the target repo as `.agent-docs/`.
10. Ask for response style preference and record it in `USER_PREFERENCES.md`.
11. Fill `QUALITY_GATES.md`, the architecture index, and ADR header.
12. Run `analyze_repo_capabilities` and record the manifest.
13. Start the auto-context file for the current task.
14. Run the architecture mapping protocol.
15. Record the bootstrap in the Action Log.
16. Initialize `HANDOFF.md`, `BACKLOG.md`, and `INDEX.md`.
17. Review `LINE_BUDGETS.yaml` for file size limits.

## Installer Mode
- If the user says "make my repository autonomous", run `autonomy_kickoff`.
- Ask only the response style, then proceed end-to-end.

## Safety
- If `AGENTS.md` or `.agent-docs/` already exist, use merge protocol by default.
- Confirm `.agentignore` covers sensitive files and production configs.
- Avoid renames or deletes unless explicitly requested.
- Keep the auto-context file free of secrets.
- Record key decisions in the ADR log.
- Follow the merge protocol for idempotent updates.
- If `.codex/skills/` already exists, run `skills_auditor` and `skills_sync`.
- For autonomy requests, avoid extra questions beyond response style.
