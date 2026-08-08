# Dependency upgrade

> Workspace: **polyglot-workspace** · Skill: `workspai-dependency-upgrade`

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
