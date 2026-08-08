---
description: Assess Workspai release readiness from evidence
---

Assess whether this workspace is release-ready using Workspai gates.

Read first:

- `.workspai/reports/INDEX.json`
- `.workspai/reports/workspace-context-agent.json`
- Any report referenced by the current blocker or task

Return:

1. Readiness verdict with cited reports
2. Blocking gates
3. Safe next command
4. Verification checklist

Use the standard Workspai answer contract: Scope, Evidence, Diagnosis, Fix Plan, Run, Verify, Assumptions.
