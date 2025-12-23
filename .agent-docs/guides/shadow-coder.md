# Shadow Coder Guide

Shadow Coder enables safe, parallel architecture experiments using a
strangler-fig approach.

## Workflow
1. Create a parallel path (e.g. `_next_gen/`).
2. Mirror interfaces without changing current behavior.
3. Validate the new path with tests or benchmarks.
4. Plan gradual migration and rollback steps.

## Safety
- Never route production traffic to the new path without proof.
- Document the migration plan in an ADR.
