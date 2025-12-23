# Agentic Operations Architect

Agentic Operations Architect is a documentation kit and set of playbooks that
turn any repository into a PhD-level autonomous software architect workspace.
It focuses on governance, proof-driven changes, decision memory, and
architecture mapping with safe automation.

## Quick Start
1. Copy `templates/AGENTS.md` into your repo root as `AGENTS.md`.
2. Copy `templates/META_INSTRUCTIONS.md` into your repo root.
3. Copy `templates/.agentignore` into your repo root.
4. Copy `templates/ARCHITECTURE.md` into your repo root.
5. Copy `templates/PLANS.md` into your repo root.
6. Copy `templates/.codex/skills/` into your repo as `.codex/skills/`.
7. Copy `templates/agent-docs/` into your repo as `.agent-docs/`.
8. Follow `guides/bootstrap.md` and `guides/architecture-mapping.md`.

## Repository Layout
- `guides/`: step-by-step playbooks for bootstrap, mapping, and governance.
- `templates/`: drop-in templates for `AGENTS.md`, `ARCHITECTURE.md`,
  `META_INSTRUCTIONS.md`, `.agentignore`, and `.agent-docs/`.
- `templates/.codex/skills/`: Codex-native skills (`SKILL.md` format).
- `checklists/`: validation lists for mapping completeness and safety checks.

## Recommended Reading Order
1. `guides/bootstrap.md`
2. `guides/governance.md`
3. `guides/architecture-mapping.md`
4. `guides/trust-layer-tdd.md`
5. `guides/repo-capabilities.md`
6. `guides/merge-protocol.md`
7. `guides/action-log.md`
8. `guides/commands-manifest.md`
9. `guides/execplan.md`
10. `guides/codex-skills.md`
11. `guides/safety-validation.md`
12. `guides/full-auth.md`
13. `guides/handoff.md`
14. `guides/backlog.md`

## Additional Guides
- `guides/decision-memory.md`
- `guides/shadow-coder.md`
- `guides/ast-injection.md`
- `guides/auto-context.md`
- `guides/large-file-partitioning.md`
- `guides/pattern-mining.md`

## Core Layers
- Safety Layer: forbidden zones via `.agentignore` and pre-commit validation.
- Trust Layer: test-first changes, auto-debug, and proof of correctness.
- Decision Memory: ADRs for major architectural choices.
- Cartography: living architecture maps that stay current.
- Auto-Context: long-run memory for large or multi-step tasks.
- Action Ledger: auditable record of actions and evidence.
- Pattern Mining: extracts automation candidates.
- ExecPlan: structured planning for large tasks.
- Handoff: compact continuity snapshot.
- Backlog: high-value follow-ups and gaps.

## Core Skills
- Cartographer: builds and updates `ARCHITECTURE.md`.
- Archaeologist: detects legacy patterns and consistency trade-offs.
- Shadow Coder: builds safe parallel architectures (strangler fig).
- Handoff Writer: keeps `HANDOFF.md` up to date.
- Backlog Curator: maintains follow-ups in `BACKLOG.md`.
- Full Auth: opt-in end-to-end execution mode.

## Codex Alignment
- Root `AGENTS.md` stays minimal with modular overrides.
- Codex-native skills live in `.codex/skills/`.
- Merge protocol keeps bootstraps idempotent.

## What It Enables
- Safe, repeatable architecture mapping with explicit confidence and gaps.
- Long-run continuity via task-scoped auto-context files.
- Evidence-backed changes with tests and ADRs.
- Idempotent bootstrapping and Codex-native skill activation.
