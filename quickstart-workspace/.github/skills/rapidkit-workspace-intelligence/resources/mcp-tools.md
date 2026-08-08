# MCP Tool Design

Workspai MCP is a read-mostly bridge over contract-validated workspace artifacts.

Candidate read tools:
- `getWorkspaceModel` — read `.workspai/reports/workspace-model.json`.
- `getWorkspaceKnowledgeGraph` — read `.workspai/reports/workspace-knowledge-graph.json`.
- `getWorkspaceEvaluation` — read `.workspai/reports/workspace-intelligence-evaluation-last-run.json` (or the live evaluation when requested).
- `queryWorkspaceEntities` — filter proof-backed graph entities by kind.
- `searchWorkspaceGraph` — retrieve bounded proof-backed context by text query.
- `getWorkspaceGraphEvidence` — resolve evidence for an entity or relation.
- `findWorkspaceGraphPath` — find a shortest proof-carrying relationship path.
- `getEvidenceIndex` — read `.workspai/reports/INDEX.json`.
- `getBlockers` — derive current blockers from INDEX and gate reports.
- `getSafeCommands` — read safe commands from `workspace-context-agent.json`.
- `getProjectContext` — return one project-scoped slice of the workspace model.
- `getArtifact` — read one explicit artifact path inside the workspace root.
- `listOperationalSkills` — read `.workspai/reports/workspace-skills-index.json`.
- `getWorkspaceExplain` — read/build workspace explain for release-blocked or project scope.
- `refreshWorkspaceIntelligence` — explicit user-approved refresh command only.

Write or repair tools require explicit approval boundaries and are intentionally not part of the first read-mostly design.
