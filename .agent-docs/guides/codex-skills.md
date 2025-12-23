# Codex Skills Guide

Codex-native skills live under `.codex/skills/<skill-name>/SKILL.md` and use
YAML frontmatter (`name`, `description`). This repo keeps a dual layer:

- `.agent-docs/skills/` for documentation.
- `.codex/skills/` for native skill activation.

## Usage
- Copy `.agent-docs/templates/.codex/skills/` into the target repo as `.codex/skills/`.
- Keep skill instructions concise and focused.
- Use `full_auth` only when explicitly authorized.
- See `.agent-docs/templates/.codex/skills/README.md` for the current skill list.
- Record audits in `.agent-docs/memory/SKILLS_STATUS.md`.
