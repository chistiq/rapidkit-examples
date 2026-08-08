# Dependency upgrade

> Workspace: **quickstart-workspace** · Skill: `workspai-dependency-upgrade`

## Objective

Upgrade dependencies with graph-aware verification.

## Triggers

- upgrade dependency
- bump package
- security advisory
- outdated deps

## Required evidence (read first)

- `.workspai/reports/INDEX.json`
- `.workspai/reports/workspace-context-agent.json`
- `.workspai/reports/workspace-verify-last-run.json`

## Procedure

1. Scope the upgrade to the owning project from workspace model.
2. Check transitive dependents via workspace graph / impact reports.
3. Prefer workspace run test/build for affected projects.
4. Re-run `workspace verify` after evidence refresh.

## Scoped projects

- ecommerce-api
- product-api

## Contract context

- **ecommerce-api**: owns `none`; publishes `none`; consumes `none`
- **product-api**: owns `none`; publishes `none`; consumes `none`

## Verification commands (this workspace)

- `npx workspai workspace verify --json`
- `npx workspai doctor workspace --json`

## Answer contract

Return: Scope, Evidence, Diagnosis, Fix Plan, Run, Verify, Assumptions.

## Refresh stale evidence

```bash
npx workspai workspace agent-sync --write --refresh-context
```
