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

Prefer manual setup? Start with `.agent-docs/guides/bootstrap.md`.

## Installer Prompt (Recommended)
This runs the full autonomy installer, maps architecture, then asks if you want
to start refactoring:

```
Make my repository autonomous with https://github.com/CheekyCodexConjurer/agentic-operations-architect.
Use autonomy_kickoff. Ask only for response style.
After mapping, ask if I want to start refactoring.
Proceed end-to-end unless blocked.
```

## Autonomy Mode (Zero Prompts)
If `.agent-docs/memory/AUTONOMY_MODE.md` is set to `auto` and `pending`, the
agent should run the installer automatically on first contact.

## Agent Management (Auto)
The kit can auto-manage multiple agents with a registry and proposals. Use:

```
Run agent_manager. Keep AGENTS_REGISTRY updated and propose new agents for uncovered domains.
```

## Update The Kit
Use the update guide or this prompt:

```
Check for upstream updates from https://github.com/CheekyCodexConjurer/agentic-operations-architect.
Compare with .agent-docs/memory/KIT_VERSION.md.
If updates exist, apply non_destructive_bootstrap using the merge protocol.
Sync .agent-docs/, .codex/skills/, and templates.
Run skills_auditor and skills_sync.
Update INDEX.md, SKILLS_STATUS.md, and ACTION_LOG with evidence.
Write the new commit hash and date to KIT_VERSION.md.
```

Example prompt: `.agent-docs/examples/update/UPDATE_PROMPT.md`.

## Continue In A New Chat
Paste this to resume work:

```
Make my repository autonomous with https://github.com/CheekyCodexConjurer/agentic-operations-architect.
Continue from .agent-docs/memory/HANDOFF.md.
Response style: technical.
Proceed end-to-end unless blocked.
```

## Repository Layout
- Root is intentionally minimal; see `.agent-docs/INDEX.md` for navigation.
- `.agent-docs/`: all documentation, templates, examples, and checklists.
- `.agent-docs/guides/`: step-by-step playbooks for bootstrap, mapping, and governance.
- `.agent-docs/templates/`: drop-in templates for `AGENTS.md`, `ARCHITECTURE.md`,
  `META_INSTRUCTIONS.md`, `.agentignore`, and `.agent-docs/`.
- `.agent-docs/templates/.codex/skills/`: Codex-native skills (`SKILL.md` format).
- `.agent-docs/checklists/`: validation lists for mapping completeness and safety checks.
- `.agent-docs/examples/`: minimal filled-in examples for reference.

## Recommended Reading Order
1. `.agent-docs/guides/bootstrap.md`
2. `.agent-docs/guides/governance.md`
3. `.agent-docs/guides/architecture-mapping.md`
4. `.agent-docs/guides/trust-layer-tdd.md`
5. `.agent-docs/guides/repo-capabilities.md`
6. `.agent-docs/guides/merge-protocol.md`
7. `.agent-docs/guides/action-log.md`
8. `.agent-docs/guides/commands-manifest.md`
9. `.agent-docs/guides/execplan.md`
10. `.agent-docs/guides/codex-skills.md`
11. `.agent-docs/guides/safety-validation.md`
12. `.agent-docs/guides/full-auth.md`
13. `.agent-docs/guides/handoff.md`
14. `.agent-docs/guides/backlog.md`
15. `.agent-docs/guides/context-compaction.md`
16. `.agent-docs/guides/command-guard.md`
17. `.agent-docs/guides/quality-gates.md`
18. `.agent-docs/guides/repo-indexer.md`
19. `.agent-docs/guides/impact-analysis.md`
20. `.agent-docs/guides/size-guard.md`
21. `.agent-docs/guides/skills-maintenance.md`
22. `.agent-docs/guides/response-style.md`
23. `.agent-docs/guides/clarify-first.md`

## Additional Guides
- `.agent-docs/guides/decision-memory.md`
- `.agent-docs/guides/shadow-coder.md`
- `.agent-docs/guides/ast-injection.md`
- `.agent-docs/guides/auto-context.md`
- `.agent-docs/guides/large-file-partitioning.md`
- `.agent-docs/guides/pattern-mining.md`

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
A: See `.agent-docs/examples/minimal/CLARIFY_FIRST_EXAMPLE.md`.

Q: Will the agent ask a lot of questions?
A: No. In autonomy mode it asks only the response style, then proceeds unless
blocked.

Q: Does autonomy include architecture mapping and a refactor prompt?
A: Yes. The installer runs mapping, then asks if you want to start refactoring.
