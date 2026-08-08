# Release readiness

> Workspace: **saas-starter-workspace** · Skill: `workspai-release-readiness`

## Objective

Assess whether this workspace is release-ready using governed Workspai gates.

## Triggers

- release
- ship
- production
- readiness gate

## Required evidence (read first)

- `.workspai/reports/INDEX.json`
- `.workspai/reports/workspace-context-agent.json`
- `.workspai/reports/workspace-verify-last-run.json`

## Procedure

1. Read `.workspai/reports/release-readiness-last-run.json` and `pipeline-last-run.json`.
2. Read `.workspai/reports/workspace-verify-last-run.json` for verdict and blocking reasons.
3. Read `.workspai/reports/artifact-remediation-plan-last-run.json` when a Studio or agent repair path is needed.
4. List blocking gates first; never claim ready without cited report fields.
5. Provide one safe next command and a verification checklist.

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
