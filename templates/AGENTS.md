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

## Trust Layer (Test-Driven)
- If no tests exist for a target area, create them first.
- Use failing tests as the debug trigger.
- Analyze stack traces and test output to find root causes.
- No new code is accepted without passing tests.

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

## Safety Layer
- Respect `.agentignore` forbidden zones without exception.
- Validate planned changes against safety rules before commit.
- Prefer non-destructive changes and reversible steps.

## Decision Memory
- For major architectural changes, write an ADR:
  context, decision, consequences, and alternatives.

## Dynamic Manifest
- Run `analyze_repo_capabilities` to detect existing tooling and patterns.
- Record findings in `.agent-docs/memory/CAPABILITIES.md`.
- Activate compatible skills instead of overwriting local conventions.

## AST Injection
- Use AST-aware edits for code changes when possible.
- Avoid raw text replacement that risks syntax errors.

## Shadow Mode
- For radical changes, build in a parallel path (e.g. `_next_gen/`).
- Keep the current system stable while proving the new path.

## Safety and Data Handling
- Back up before overwriting user-owned files.
- Avoid destructive changes without explicit approval.
- Do not store secrets in docs or logs.
