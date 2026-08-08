<!-- RAPIDKIT:AGENT-GROUNDING:START -->
# Workspai agent grounding

Cross-tool instructions for Copilot, Cursor, Claude Code, Codex, Grok, and other agents.

## Read order (mandatory before workspace diagnosis)

1. `.workspai/reports/INDEX.json` — latest blockers, timestamps, and report paths
2. `.workspai/reports/workspace-context-agent.json` — read only task-relevant context
3. Read only the task-relevant evidence artifacts listed in the index.
4. Use `workspace graph search <query> --limit 12 --json` or MCP `searchWorkspaceGraph` before loading the full graph.

Do **not** full-repo scan or inject the complete graph when a bounded query can answer the task.

## Regenerate intelligence

```bash
npx workspai workspace agent-sync --write --refresh-context
npx workspai workspace context --for-agent --json --write
npx workspai pipeline --json --write
```

## Safe commands (prefer these)

- `npx workspai workspace model --json` — Read the canonical workspace intelligence model.
- `npx workspai workspace graph entities --json` — Query proof-backed workspace entities without loading the full graph.
- `npx workspai workspace graph evidence <entity-or-relation> --json` — Resolve portable evidence for a graph entity or relation.
- `npx workspai workspace graph path <from> <to> --json` — Find a shortest proof-carrying path between workspace entities.
- `npx workspai doctor workspace --json` — Check workspace health before claiming verification.
- `npx workspai pipeline --json` — Run the governed sync, doctor, analyze, readiness, and autopilot loop.
- `npx workspai workspace contract verify --json` — Verify workspace contract and dependency edges.
- `npx workspai workspace verify --json` — Evaluate evidence freshness and verification gates before release decisions.

## Rules

- Treat `.workspai/reports/*` as the source of truth for health, gates, and release posture.
- Prefer deterministic Workspai CLI commands over heuristic framework guesses.
- If evidence is missing or stale, run the refresh commands above before proposing fixes.
- Keep project-scoped advice aligned with the active project named in the context pack.
<!-- RAPIDKIT:AGENT-GROUNDING:END -->
