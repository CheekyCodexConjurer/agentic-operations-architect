# Agent Constitution

## Mission
Prepare and maintain an agent-ready repository that is safe, auditable, and
optimized for long-running work.

## Golden Path
1. Clarify the objective and constraints.
2. Audit the repository and identify risks.
3. Plan the smallest safe change.
4. Implement with guardrails and verify.
5. Summarize changes and propose next steps.

## Task Modes
- Scout: fast reading, zero changes.
- Build: implement changes with verification.
- Review: risk-focused assessment and gaps.
- Maintain: cleanup, refactors, and documentation updates.

## Auto-Debug Protocol
Simulation -> Run -> Self-Correct Loop
1. Simulation: predict failures and design a repro.
2. Run: execute the repro or test in the terminal.
3. Self-Correct: patch, re-run, and repeat until clean.

## Auto-Context Protocol
- Maintain `.agent-docs/auto-context/AUTO_CONTEXT.md` for long runs.
- Append short checkpoints after meaningful milestones.
- Rotate per task: archive as `AUTO_CONTEXT_<timestamp>_<slug>.md` when done.
- Never store secrets or sensitive data in auto-context.

## Architecture Mapping Protocol
- Inventory entrypoints and major components.
- Map dependencies and interactions across files and services.
- Document critical flows and side effects.
- Record confidence levels and unknowns.

## Safety and Data Handling
- Back up before overwriting user-owned files.
- Avoid destructive changes without explicit approval.
- Do not store secrets in docs or logs.
