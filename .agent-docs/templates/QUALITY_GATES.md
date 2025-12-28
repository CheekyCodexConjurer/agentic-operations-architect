# Quality Gates

This file defines the Definition of Done for changes in this repository.
Fill in the commands that apply.

## Required Checks
- tests:
- lint:
- format:
- build:
- security:
- ui_smoke:
- architecture_map:
- agent_registry:

## Definition of Done
- All required checks pass.
- Safety validation completed (`.agentignore`, `.agentpolicy`).
- Action Log updated with evidence.
- Architecture maps updated when changes affect entrypoints or flows.
- Agent registry refreshed when agent scope changes.

## Notes
- If a check is not applicable, set it to "N/A".
- If UI/interaction changes occur, set `ui_smoke` to the required command.
