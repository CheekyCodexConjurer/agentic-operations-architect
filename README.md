# Agentic Operations Architect

Agentic Operations Architect is a documentation kit and set of playbooks that
help any repository become agent-ready. It defines governance, architecture
mapping protocols, auto-context rules for long runs, and reusable templates.

## Quick Start
1. Copy `templates/AGENTS.md` into your repo root as `AGENTS.md`.
2. Copy `templates/agent-docs/` into your repo as `.agent-docs/`.
3. Follow `guides/bootstrap.md` and `guides/architecture-mapping.md`.

## Repository Layout
- `guides/`: step-by-step playbooks for bootstrap, mapping, and governance.
- `templates/`: drop-in templates for AGENTS, architecture, ADRs, skills, and
  auto-context.
- `checklists/`: validation lists for mapping completeness.

## What It Enables
- Safe, repeatable architecture mapping with explicit confidence and gaps.
- Long-run continuity via task-scoped auto-context files.
- Clear governance and decision tracking through ADRs.
