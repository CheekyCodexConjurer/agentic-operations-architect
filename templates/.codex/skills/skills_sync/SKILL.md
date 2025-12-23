---
name: skills_sync
description: Align Codex-native skills with documented skills safely.
metadata:
  short-description: Skills sync
---

## Purpose
Ensure `.codex/skills/` matches `.agent-docs/skills/`.

## Steps
1. Check for missing skills in either location.
2. Add missing entries using merge protocol.
3. Validate frontmatter and folder naming.
4. Update `.agent-docs/memory/SKILLS_STATUS.md`.

## Guardrails
- Avoid overwriting existing skill content.
