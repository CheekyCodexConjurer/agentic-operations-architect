# Bootstrap Guide

Use this guide to prepare any repository for agentic work using the templates
and protocols in this repo.

## Steps
1. Copy `templates/AGENTS.md` into the target repo root as `AGENTS.md`.
2. Copy `templates/agent-docs/` into the target repo as `.agent-docs/`.
3. Fill the architecture index and ADR header with known facts.
4. Start the auto-context file for the current task.
5. Run the architecture mapping protocol.

## Safety
- If `AGENTS.md` or `.agent-docs/` already exist, archive them with a timestamp.
- Back up or rename existing agent docs before overwriting.
- Keep the auto-context file free of secrets.
- Record key decisions in the ADR log.
