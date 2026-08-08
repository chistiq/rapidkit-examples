# Diagnose API failure

> Workspace: **python-only-workspace** · Skill: `workspai-diagnose-api-failure`

## Objective

Investigate a failing API or service using Workspai evidence before editing application code.

## Triggers

- api failure
- 500 error
- integration test failed
- service unreachable

## Required evidence (read first)

- `.workspai/reports/INDEX.json`
- `.workspai/reports/workspace-context-agent.json`
- `.workspai/reports/workspace-verify-last-run.json`

## Procedure

1. Read `.workspai/reports/INDEX.json` and identify fail/warn reports for the scoped project.
2. Read `.workspai/reports/doctor-last-run.json`, `doctor-project-last-run.json`, and project-scoped run evidence if present.
3. If a fix was requested, read `artifact-remediation-plan-last-run.json` for cross-artifact next steps, then `doctor-remediation-plan-last-run.json` for Doctor-specific file edits.
4. Map the failure to workspace vs project scope; cite exit codes and blocker messages.
5. Propose the smallest safe fix (config, env, dependency) with explicit verification commands.

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
