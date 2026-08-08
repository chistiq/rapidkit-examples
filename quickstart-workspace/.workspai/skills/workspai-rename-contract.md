# Rename contract safely

> Workspace: **quickstart-workspace** · Skill: `workspai-rename-contract`

## Objective

Rename or change a shared contract with consumer awareness.

## Triggers

- rename contract
- rename event
- breaking api
- contract change

## Required evidence (read first)

- `.workspai/reports/INDEX.json`
- `.workspai/reports/workspace-context-agent.json`
- `.workspai/reports/workspace-verify-last-run.json`

## Procedure

1. Read `.workspai/workspace.contract.json` for publishes/consumes/owns edges.
2. List all consumer projects before proposing renames.
3. Update contract file and regenerate workspace model.
4. Verify contract gate and integration tests for consumers.

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
