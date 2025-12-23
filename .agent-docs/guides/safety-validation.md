# Safety Validation Guide

Before any commit or merge, validate that changes respect forbidden zones and
governance rules.

## Steps
1. Compare changed paths against `.agentignore`.
2. Confirm no forbidden files were modified.
3. If conflicts exist, stop and document in `ACTION_LOG.md`.
4. Record validation evidence in the Action Log.
