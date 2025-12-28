# Update Kit Guide

This guide keeps the automation kit aligned with upstream changes.

## Files
- `.agent-docs/memory/KIT_VERSION.md`
- `.agent-docs/memory/AGENTS_REGISTRY.md`
- `.agent-docs/memory/SKILLS_STATUS.md`
- `.agent-docs/memory/INDEX.md`

## Workflow
1. Read `KIT_VERSION.md` for current version metadata.
2. Compare to upstream release or commit.
3. Apply `non_destructive_bootstrap` using merge protocol.
4. Run `skills_auditor` and `skills_sync`.
5. Refresh indexes and record in Action Log.
6. Update `KIT_VERSION.md` with new version data.
7. Use the update kit checklist for completeness.

## Notes
- Preserve fixed agents and local overrides.
- Use `.agent-docs/compat/` for conflicts.
