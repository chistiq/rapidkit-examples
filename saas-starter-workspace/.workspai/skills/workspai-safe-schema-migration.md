# Safe schema migration

> Workspace: **saas-starter-workspace** · Skill: `workspai-safe-schema-migration`

## Objective

Plan and verify a schema migration with blast-radius awareness.

## Triggers

- migration
- schema change
- database migration
- db migrate

## Required evidence (read first)

- `.workspai/reports/INDEX.json`
- `.workspai/reports/workspace-context-agent.json`
- `.workspai/reports/workspace-verify-last-run.json`

## Procedure

1. Identify affected projects from workspace model and dependency graph.
2. Run or review impact/verify evidence for transitive dependents.
3. Require project-scoped test/build commands before promoting the migration.
4. Document rollback and verification signals.

## Scoped projects

- saas-admin
- saas-api
- saas-nest
- saas-webhooks

## Contract context

- **saas-admin**: owns `none`; publishes `none`; consumes `none`
- **saas-api**: owns `none`; publishes `none`; consumes `none`
- **saas-nest**: owns `none`; publishes `none`; consumes `none`
- **saas-webhooks**: owns `none`; publishes `none`; consumes `none`

## Verification commands (this workspace)

- `npx workspai workspace verify --json`
- `npx workspai doctor workspace --json`

## Answer contract

Return: Scope, Evidence, Diagnosis, Fix Plan, Run, Verify, Assumptions.

## Refresh stale evidence

```bash
npx workspai workspace agent-sync --write --refresh-context
```
