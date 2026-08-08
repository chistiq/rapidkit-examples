# Safe schema migration

> Workspace: **enterprise-workspace** · Skill: `workspai-safe-schema-migration`

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

## Verification commands (this workspace)

- `npx workspai workspace model --json`
- `npx workspai workspace graph entities --json`
- `npx workspai workspace graph evidence <entity-or-relation> --json`
- `npx workspai workspace graph path <from> <to> --json`
- `npx workspai doctor workspace --json`
- `npx workspai pipeline --json`
- `npx workspai workspace contract verify --json`
- `npx workspai workspace verify --json`

## Answer contract

Return: Scope, Evidence, Diagnosis, Fix Plan, Run, Verify, Assumptions.

## Refresh stale evidence

```bash
npx workspai workspace agent-sync --write --refresh-context
```
