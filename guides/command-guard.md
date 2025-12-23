# Command Guard Guide

Command Guard enforces safe execution rules before running commands.

## File
- `.agentpolicy`

## Workflow
1. Read `.agentpolicy` before executing commands.
2. Deny commands listed under `deny`.
3. Require explicit confirmation for `confirm`.
4. Record the decision in `ACTION_LOG.md`.
