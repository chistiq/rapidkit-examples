# Workspai agent grounding
Generated: 2026-08-08T20:32:59.189Z
This file is tool-agnostic. Synced agents should read it together with `.workspai/reports/INDEX.json`.
## Mandatory read order
1. `.workspai/reports/workspace-context-agent.json`
2. `.workspai/reports/workspace-verify-last-run.json`
3. `.workspai/reports/workspace-impact-last-run.json`
4. `.workspai/reports/workspace-explain-last-run.json`
5. `.workspai/reports/workspace-model.json`
6. `.workspai/reports/workspace-knowledge-graph.json`
7. `.workspai/reports/workspace-skills-index.json`
8. `.workspai/reports/workspace-intelligence-evaluation-last-run.json`
9. `.workspai/reports/doctor-last-run.json`
10. `.workspai/reports/doctor-project-last-run.json`
11. `.workspai/reports/doctor-remediation-plan-last-run.json`
12. `.workspai/reports/artifact-remediation-plan-last-run.json`
13. `.workspai/reports/doctor-fix-result-last-run.json`
14. `.workspai/reports/analyze-last-run.json`
15. `.workspai/reports/pipeline-last-run.json`
16. `.workspai/reports/release-readiness-last-run.json`
17. `.workspai/reports/workspace-model-snapshot.json`
18. `.workspai/reports/workspace-model-diff-last-run.json`
19. `.workspai/reports/workspace-contract-verify-last-run.json`
20. `.workspai/reports/workspace-intelligence-history.json`
## Refresh
```bash
npx workspai workspace agent-sync --write --refresh-context
```
