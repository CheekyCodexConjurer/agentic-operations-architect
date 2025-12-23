# Repo Capabilities Guide

This guide defines the dynamic manifest step (`analyze_repo_capabilities`).
The goal is to detect existing tooling and adapt, not overwrite.

## Signals to Detect
- CI/CD: `.github/workflows`, `gitlab-ci.yml`, `azure-pipelines.yml`
- Containers: `Dockerfile`, `docker-compose.yml`
- IaC: `terraform`, `pulumi`, `cloudformation`
- Agents: `AGENTS.md`, `.agent-docs/`, `agents/`
- Frameworks: `package.json`, `pyproject.toml`, `go.mod`, `pom.xml`

## Output
- Record findings in `.agent-docs/memory/CAPABILITIES.md`.
- Activate relevant skills and protocols.
- Flag conflicts between existing conventions and new plans.
- Update `COMMANDS.md`, `COMMANDS.json`, and `MANIFEST.yaml` when possible.
