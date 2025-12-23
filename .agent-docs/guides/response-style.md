# Response Style Guide

Use this guide to set a response style that matches the user's preference.

## File
- `.agent-docs/memory/USER_PREFERENCES.md`

## Workflow
1. On first interaction, ask: "Do you prefer technical detail or humanized?"
2. Record the choice in `USER_PREFERENCES.md`.
3. Continue execution without further questions unless blocked.
4. Allow the user to change the style later.

## Humanized Mode
- Short, plain language.
- Minimal bullets and minimal code.
- Enough context to track progress, no deep internals.

## Autonomy Note
- After response style is chosen, proceed automatically.
