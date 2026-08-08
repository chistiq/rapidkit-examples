<!-- RAPIDKIT:AGENT-GROUNDING:START -->
# Workspai workspace grounding

Before answering workspace, release, or architecture questions:

1. Read `AGENTS.md` (managed Workspai section).
2. Read `.workspai/reports/INDEX.json` and only task-relevant context from `.workspai/reports/workspace-context-agent.json`.
3. Use bounded `workspace graph search` or MCP `searchWorkspaceGraph` before scanning the full repository.

Regenerate stale intelligence:

```bash
npx workspai workspace agent-sync --write --refresh-context
```
<!-- RAPIDKIT:AGENT-GROUNDING:END -->
