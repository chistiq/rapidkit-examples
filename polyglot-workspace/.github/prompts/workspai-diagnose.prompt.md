---
description: Diagnose Workspai workspace blockers from evidence reports
---

Diagnose this workspace using Workspai evidence only.

Read:

- `.workspai/reports/INDEX.json`
- `.workspai/reports/workspace-context-agent.json`
- Any fail/warn reports referenced in the index

Return:

1. Root cause grounded in report blockers
2. Smallest safe fix path (commands + file edits)
3. One verification command to prove recovery
