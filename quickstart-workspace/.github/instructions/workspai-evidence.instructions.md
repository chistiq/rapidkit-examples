---
applyTo: ".workspai/**,**/.workspai/**,.rapidkit/**,**/.rapidkit/**"
description: Workspai evidence and intelligence artifacts
---

When working under `.workspai/` or legacy `.rapidkit/`:

- Treat `.workspai/reports/*` JSON reports as canonical gate and health evidence.
- Start from `.workspai/reports/INDEX.json` for read order and blockers.
- Do not invent pass/fail state — cite `exitCode`, `blockers`, and `generatedAt` fields.
