# Workspai project grounding

This project is part of the **saas-starter-workspace** Workspai workspace.
Commands launched from this project resolve that workspace automatically; you do not need to change directories first.

## Start here

1. Read `.workspai/reports/project-context-agent.json` for the bounded project lens.
2. Read the workspace report index only when the task crosses the project boundary.
3. Use graph search/evidence commands instead of loading the full graph into a prompt.
4. Do not claim healthy, ready, or verified without current Workspai evidence.

The Workspace Model owns canonical project identity and its compact `projectTopology`.
The Workspace Knowledge Graph is a separate, proof-backed enrichment containing
files, symbols, APIs, infrastructure, tests, owners, and decisions. Do not treat
an unproven topology edge as proof that two projects are independent.

## Project

- Name: `saas-webhooks`
- Workspace-relative identity: `saas-webhooks`
- Runtime: `python`
- Framework: `fastapi`
- Relationship: `managed`
- Related projects: `saas-admin`, `saas-api`
- Topology status: `unproven`
- Model freshness: `unknown`
- Knowledge Graph freshness: `fresh`

## Current evidence coverage

- Project-scoped entities: 804
- Project-scoped relations: 1106
- Portable proofs: 1157

- **warning · graph.knowledge.project_relationships_unknown:** 4 project(s) have no proven inter-project relationship. This is unknown topology, not proof of independence.

## Current project blockers

- No current project-scoped blocker is recorded.

## Safe commands from this project

```bash
npx workspai project workspace status --json
npx workspai doctor project --json
npx workspai workspace graph search "saas-webhooks" --limit 12 --json
npx workspai workspace verify --strict --json
```

The machine-local workspace path lives only in `.workspai/workspace-link.local.json`, which is gitignored. Portable grounding files never publish that path.
