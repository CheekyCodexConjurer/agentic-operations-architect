# Agentic Operations Architect

Agentic Operations Architect is a documentation kit and set of playbooks that
turn any repository into a PhD-level autonomous software architect workspace.
It focuses on governance, proof-driven changes, decision memory, and
architecture mapping with safe automation.

## Quick Start
Paste this into your coding agent:

```
Make my repository autonomous with https://github.com/CheekyCodexConjurer/agentic-operations-architect
```

Prefer manual setup? Start with `guides/bootstrap.md`.

## Continue In A New Chat
Paste this to resume work:

```
Make my repository autonomous with https://github.com/CheekyCodexConjurer/agentic-operations-architect.
Continue from .agent-docs/memory/HANDOFF.md.
Response style: technical.
Proceed end-to-end unless blocked.
```

## Repository Layout
- `guides/`: step-by-step playbooks for bootstrap, mapping, and governance.
- `templates/`: drop-in templates for `AGENTS.md`, `ARCHITECTURE.md`,
  `META_INSTRUCTIONS.md`, `.agentignore`, and `.agent-docs/`.
- `templates/.codex/skills/`: Codex-native skills (`SKILL.md` format).
- `checklists/`: validation lists for mapping completeness and safety checks.
- `examples/`: minimal filled-in examples for reference.

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
15. `guides/context-compaction.md`
16. `guides/command-guard.md`
17. `guides/quality-gates.md`
18. `guides/repo-indexer.md`
19. `guides/impact-analysis.md`
20. `guides/size-guard.md`
21. `guides/skills-maintenance.md`
22. `guides/response-style.md`
23. `guides/clarify-first.md`

## Additional Guides
- `guides/decision-memory.md`
- `guides/shadow-coder.md`
- `guides/ast-injection.md`
- `guides/auto-context.md`
- `guides/large-file-partitioning.md`
- `guides/pattern-mining.md`

## Core Layers
- Safety Layer: forbidden zones via `.agentignore` and pre-commit validation.
- Command Guard: safe command execution via `.agentpolicy`.
- Trust Layer: test-first changes, auto-debug, and proof of correctness.
- Decision Memory: ADRs for major architectural choices.
- Cartography: index-first architecture maps with detailed drill-downs.
- Auto-Context: long-run memory for large or multi-step tasks.
- Action Ledger: auditable record of actions and evidence.
- Pattern Mining: extracts automation candidates.
- ExecPlan: structured planning for large tasks.
- Handoff: compact continuity snapshot.
- Backlog: high-value follow-ups and gaps.
- Quality Gates: Definition of Done with explicit checks.
- Size Guard: line budgets for context-heavy files.
- Response Style: short responses aligned to user preference.
- Clarify First: plan and confirm before coding.

## Core Skills
- Cartographer: builds and updates `ARCHITECTURE.md`.
- Archaeologist: detects legacy patterns and consistency trade-offs.
- Shadow Coder: builds safe parallel architectures (strangler fig).
- Handoff Writer: keeps `HANDOFF.md` up to date.
- Backlog Curator: maintains follow-ups in `BACKLOG.md`.
- Full Auth: opt-in end-to-end execution mode.
- Context Compactor: keeps memory concise for long runs.
- Command Guard: enforces command safety rules.
- Quality Gates: enforces Definition of Done.
- Size Guard: keeps operational files within line budgets.
- Skills Auditor: finds malformed or missing skills.
- Skills Sync: aligns `.codex/skills/` with `.agent-docs/skills/`.
- Response Style Selector: sets the preferred response style.
- Clarify First: confirms requirements before implementation.

## Codex Alignment
- Root `AGENTS.md` stays minimal with modular overrides.
- Codex-native skills live in `.codex/skills/`.
- Merge protocol keeps bootstraps idempotent.
- `.agentpolicy` and `QUALITY_GATES.md` define safety and completion.
- Index-first docs reduce context and prevent tunnel vision.
- `ARCHITECTURE.md` stays index-only; details live in `.agent-docs/architecture/`.

## What It Enables
- Safe, repeatable architecture mapping with explicit confidence and gaps.
- Long-run continuity via task-scoped auto-context files.
- Evidence-backed changes with tests and ADRs.
- Idempotent bootstrapping and Codex-native skill activation.
- Command safety and explicit Definition of Done gates.

## FAQ
Q: What is the difference between technical and humanized responses?
A: Technical responses are concise and structured with precise changes and
references. Humanized responses are short, plain language, minimal bullets, and
only the context needed to stay informed.

Q: How does "clarify first" look in practice?
A: See `examples/minimal/CLARIFY_FIRST_EXAMPLE.md`.

Q: Will the agent ask a lot of questions?
A: No. In autonomy mode it asks only the response style, then proceeds unless
blocked.

Q: Does autonomy include architecture mapping and a refactor prompt?
A: Yes. The installer runs mapping, then asks if you want to start refactoring.
