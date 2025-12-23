# Pattern Mining Guide

Pattern mining turns action logs into reusable automation and skill proposals.

## Inputs
- `.agent-docs/memory/ACTION_LOG.md`
- `.agent-docs/memory/ACTION_LOG.jsonl`

## Output
- `.agent-docs/memory/PATTERNS.md`
- `.agent-docs/memory/BACKLOG.md` (when follow-ups are needed)

## Rules
- Extract only high-signal recurring patterns.
- Propose skills, do not create them automatically.
- Link evidence from the action log.
