# Skills Maintenance Guide

This guide covers auditing and syncing Codex-native skills.

## Files
- `.codex/skills/*/SKILL.md`
- `.agent-docs/skills/`
- `.agent-docs/memory/SKILLS_STATUS.md`

## Workflow
1. Run `skills_auditor` to detect missing or malformed skills.
2. Run `skills_sync` to align `.codex/skills/` and `.agent-docs/skills/`.
3. Record findings in `SKILLS_STATUS.md`.

## Checks
- `SKILL.md` has YAML frontmatter with `name` and `description`.
- Folder names match the `name` field.
- Documentation exists for each skill.
