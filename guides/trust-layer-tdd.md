# Trust Layer (TDD) Guide

This guide enforces proof-driven development. The agent must not accept new
code unless tests are green.

## Workflow
1. Identify the behavior to change.
2. If tests are missing, create them first.
3. Run tests and capture failures.
4. Use stack traces to isolate root cause.
5. Implement the smallest fix.
6. Re-run tests until green.

## Integration with Auto-Debug
- Failing tests trigger the debug protocol.
- Debug is evidence-driven, not trial and error.
- Each loop should reduce the failure surface.
