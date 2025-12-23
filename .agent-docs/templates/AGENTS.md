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

## Instruction Chain Strategy
- Keep root `AGENTS.md` concise and modular.
- Put module-specific rules in subdirectory `AGENTS.md` files.
- Use `AGENTS.override.md` to replace rules when needed.
- Avoid overloading a single file; link to guides instead.
- Stay under instruction size limits to avoid truncation (default 32KiB).

## Context Economy
- Prefer index files that link to detailed docs.
- Load only the files needed for the current task.
- Avoid reading every document by default to prevent tunnel vision.

## Task Modes
- Scout: fast reading, zero changes.
- Build: implement changes with verification.
- Review: risk-focused assessment and gaps.
- Maintain: cleanup, refactors, and documentation updates.

## Response Style
- On first interaction, ask for preferred response style.
- Options: technical detail or humanized.
- Record the choice in `.agent-docs/memory/USER_PREFERENCES.md`.
- Keep responses short and aligned to the chosen style.

## Autonomy Installer Trigger
- If the user requests autonomy or `AUTONOMY_MODE.md` is auto/pending, run
  `autonomy_kickoff` immediately.
- Ask only for response style, then proceed end-to-end.
- Mark `AUTONOMY_MODE.md` as done when finished.

## Clarify First
- For change requests, ask clarifying questions only when blocked or high-risk.
- Default to implementation after response style is chosen.
- Skip clarification when the user requests autonomy or Full Auth.

## Refactor Gate
- After architecture mapping, ask if the user wants to refactor now.
- If yes, proceed with `PLANS.md` + `IMPACT.md`.
- If no, capture refactor ideas in `BACKLOG.md`.

## Full Auth Mode
- Use only when the user explicitly authorizes end-to-end execution.
- Produce a phased plan first, then execute all phases in one run.
- Stop only when Definition of Done is met.

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

## Merge Protocol (Idempotent)
- Never delete or rename existing agent docs by default.
- If a file exists, append or update within marked blocks only.
- If conflicts exist, add a companion note in `.agent-docs/compat/`.
- Reruns must be safe and not duplicate content.

## Action Ledger
- Record meaningful actions in `.agent-docs/memory/ACTION_LOG.md`.
- Mirror entries in `.agent-docs/memory/ACTION_LOG.jsonl` for mining.

## Handoff and Backlog
- Maintain `.agent-docs/memory/HANDOFF.md` for session resets.
- Maintain `.agent-docs/memory/BACKLOG.md` for high-value follow-ups.

## Context Compaction
- Periodically compact `AUTO_CONTEXT.md` into `HANDOFF.md`.
- Archive completed task context to keep files small.

## Size Guard
- Keep context-heavy files between 300-500 lines.
- Use `LINE_BUDGETS.yaml` to rotate or split long docs.

## Architecture Mapping Protocol
- Inventory entrypoints and major components.
- Map dependencies and interactions across files and services.
- Document critical flows and side effects.
- Record confidence levels and unknowns.
- Keep `ARCHITECTURE.md` and `.agent-docs/architecture.md` as index-only.

## Safety Layer
- Respect `.agentignore` forbidden zones without exception.
- Validate planned changes against safety rules before commit.
- Prefer non-destructive changes and reversible steps.
- Enforce `.agentpolicy` for command safety.

## Decision Memory
- For major architectural changes, write an ADR:
  context, decision, consequences, and alternatives.

## Dynamic Manifest
- Run `analyze_repo_capabilities` to detect existing tooling and patterns.
- Record findings in `.agent-docs/memory/CAPABILITIES.md`.
- Activate compatible skills instead of overwriting local conventions.
- Prefer Codex-native skills in `.codex/skills/` when available.

## Commands and Manifest
- Maintain `.agent-docs/memory/COMMANDS.md` and `COMMANDS.json`.
- Keep `.agent-docs/memory/MANIFEST.yaml` up to date.

## Repo Index and Impact
- Maintain `.agent-docs/memory/INDEX.md` and `INDEX.json`.
- Create `.agent-docs/memory/IMPACT.md` before high-risk changes.

## Skills Integrity
- Audit `.codex/skills/` for correct structure.
- Sync with `.agent-docs/skills/` using merge protocol.

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

## ExecPlan for Long Tasks
- Use `PLANS.md` for multi-hour or high-risk changes.
- Track progress and verification explicitly.

## Quality Gates
- Use `QUALITY_GATES.md` as the Definition of Done.
- Do not mark work complete without recorded evidence.
