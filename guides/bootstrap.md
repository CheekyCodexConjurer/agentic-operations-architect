# Bootstrap Guide

Use this guide to prepare any repository for agentic work using the templates
and protocols in this repo.

## Steps
1. Copy `templates/AGENTS.md` into the target repo root as `AGENTS.md`.
2. Copy `templates/META_INSTRUCTIONS.md` into the target repo root.
3. Copy `templates/.agentignore` into the target repo root.
4. Copy `templates/ARCHITECTURE.md` into the target repo root.
5. Copy `templates/agent-docs/` into the target repo as `.agent-docs/`.
6. Fill the architecture index and ADR header with known facts.
7. Run `analyze_repo_capabilities` and record the manifest.
8. Start the auto-context file for the current task.
9. Run the architecture mapping protocol.

## Safety
- If `AGENTS.md` or `.agent-docs/` already exist, archive them with a timestamp.
- Confirm `.agentignore` covers sensitive files and production configs.
- Back up or rename existing agent docs before overwriting.
- Keep the auto-context file free of secrets.
- Record key decisions in the ADR log.
