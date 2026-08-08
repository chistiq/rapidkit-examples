---
applyTo: "**"
description: Workspai workspace scope, evidence, and command discipline
---

# Workspai Workspace Intelligence

Use Workspai reports as the workspace source of truth before giving architectural, repair, release, or project lifecycle advice.

## Scope rules

- Start from `.workspai/reports/INDEX.json`; read only task-relevant context and evidence.
- Prefer bounded `workspace graph search` or MCP `searchWorkspaceGraph` over loading the complete graph.
- Distinguish workspace-level blockers from project-level blockers.
- When a project is active, cite its name, path, framework, and evidence source.
- Do not translate unsupported stack requests into unrelated native kits.

## Answer contract

Return answers with: Scope, Evidence, Diagnosis, Fix Plan, Run, Verify, Assumptions.
