# Architecture Overview

This repository is a documentation-only system that defines how an autonomous
PhD-level software architect should operate inside any target codebase. It
ships governance rules, mapping protocols, and reusable templates.

## System Goal
Enable safe, auditable, and high-fidelity software changes by enforcing
governance, proof-driven development, and living architecture maps.

## Core Layers
- Safety Layer: forbidden zones, pre-commit validation, and non-destructive
  workflows.
- Command Guard: safe command execution via `.agentpolicy`.
- Trust Layer: test-first changes and auto-debug until proof is obtained.
- Decision Memory: ADRs that justify architectural choices.
- Cartography: living architecture maps and interaction graphs.
- Auto-Context: task-scoped continuity for long runs.
- Action Ledger: auditable record of changes and evidence.
- Pattern Mining: extract recurring operations into automation proposals.
- ExecPlan: structured planning for long or risky tasks.
- Quality Gates: explicit Definition of Done checks.

## Key Artifacts
- `AGENTS.md`: constitution and protocols.
- `META_INSTRUCTIONS.md`: agent priorities and philosophy.
- `ARCHITECTURE.md`: baseline architecture map for the target repo.
- `PLANS.md`: exec plan for large changes.
- `QUALITY_GATES.md`: Definition of Done for checks.
- `.agentignore`: forbidden zones the agent must never modify.
- `.agentpolicy`: command guard rules.
- `.agent-docs/architecture.md`: architecture index.
- `.agent-docs/architecture/*.md`: interaction maps, flow maps, component
  profiles.
- `.agent-docs/compat/`: supplemental notes when merging is blocked.
- `.agent-docs/memory/DECISIONS.md`: ADR log.
- `.agent-docs/memory/ACTION_LOG.md`: action ledger (human).
- `.agent-docs/memory/ACTION_LOG.jsonl`: action ledger (machine).
- `.agent-docs/memory/PATTERNS.md`: mined automation patterns.
- `.agent-docs/memory/COMMANDS.md`: best-known commands.
- `.agent-docs/memory/COMMANDS.json`: machine commands.
- `.agent-docs/memory/MANIFEST.yaml`: machine-readable repo manifest.
- `.agent-docs/memory/CAPABILITIES.md`: capability detection log.
- `.agent-docs/memory/HANDOFF.md`: compact state snapshot for session resets.
- `.agent-docs/memory/BACKLOG.md`: high-value follow-ups and gaps.
- `.agent-docs/memory/INDEX.md`: repo navigation index.
- `.agent-docs/memory/INDEX.json`: machine index.
- `.agent-docs/memory/IMPACT.md`: change impact analysis.
- `.agent-docs/auto-context/AUTO_CONTEXT.md`: task-scoped context log.
- `.agent-docs/skills/*.md`: skill playbooks for specialized behaviors.
- `.codex/skills/*/SKILL.md`: Codex-native skill definitions.

## Interactions and Flow
1. Bootstrap copies the templates into a target repo.
2. The agent reads `AGENTS.md` and `META_INSTRUCTIONS.md` to set priorities.
3. `analyze_repo_capabilities` scans for existing tooling and patterns.
4. Repo Indexer builds `INDEX.md` and `INDEX.json`.
5. The Cartographer maps entrypoints, components, and flows.
6. Impact Analyzer documents risk in `IMPACT.md` for planned changes.
7. The Trust Layer enforces TDD, then uses auto-debug on failures.
8. The Command Guard checks `.agentpolicy` before running commands.
9. The Safety Layer validates that no forbidden paths were touched.
10. Action Ledger records changes and verification evidence.
11. Decision Memory captures major architectural changes in ADRs.
12. Auto-context maintains state for long runs and rotates per task.
13. Handoff Writer captures compact state for session continuity.
14. Backlog Curator records gaps and follow-ups.
15. Pattern Mining proposes automations for future runs.
16. Quality Gates validate Definition of Done.

## Safety Layer
- `.agentignore` defines protected files and directories.
- Pre-commit validation checks modifications against forbidden zones.
- Shadow Coder supports parallel architecture changes without breakage.
- Merge protocol keeps changes idempotent.
- `.agentpolicy` guards risky commands.

## Trust Layer
- Tests are required before changes in a target area.
- Failures trigger structured debug and root-cause analysis.
- No new code is accepted without passing tests.

## Decision Memory
- Every architectural change receives an ADR with context, decision, and
  consequences.

## Action Ledger
- Record all meaningful changes and commands.
- Keep evidence for tests and checks.

## ExecPlan
- Use `PLANS.md` to guide multi-hour or high-risk work.

## Quality Gates
- Use `QUALITY_GATES.md` to define required checks.

## Universal Adaptation
- The agent detects repo signatures to activate relevant skills.
- Changes should use AST-based insertion when possible, not raw text edits.

## Codex Alignment
- Keep root instructions small and modular to avoid truncation.
- Prefer Codex-native skills under `.codex/skills/` when present.
