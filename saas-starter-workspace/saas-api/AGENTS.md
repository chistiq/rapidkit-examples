<!-- WORKSPAI:PROJECT-GROUNDING:START -->
# Workspai project boundary

- Project: `saas-api`
- Canonical workspace: `saas-starter-workspace`
- Portable project lens: `.workspai/reports/project-context-agent.json`
- Project grounding: `.workspai/PROJECT-GROUNDING.md`
- Workspace discovery: run `npx workspai project workspace status --json`

For project-local tasks, start with the project lens. When a change can affect another project, a contract, an API, infrastructure, or release readiness, follow the workspace evidence references and query the Workspai graph. The agent should run the bounded graph search/evidence commands itself when required; the user does not need to preload the full graph. `projectTopology` is the compact project dependency view in the canonical Workspace Model, while the Workspace Knowledge Graph is the proof-backed detail layer. Workspai commands launched here resolve the canonical workspace automatically. Never copy the machine-local workspace link into answers, commits, or generated portable artifacts.
<!-- WORKSPAI:PROJECT-GROUNDING:END -->
