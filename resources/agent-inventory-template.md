# Agent Inventory Template

Keep one row per managed agent. Do not store API keys, passwords, tokens, or other secrets in this inventory.

| Agent name | Purpose / task | Workspace | Owner | Status | Plugins | Last reviewed | Notes |
|---|---|---|---|---|---|---|---|
| | | | | | | | |
| | | | | | | | |
| | | | | | | | |

## Agent Detail Record

Duplicate this section when an agent needs a fuller record.

- **Agent name:**
- **Purpose:**
- **Primary owner:**
- **Workspace path:**
- **Current status:**
- **Required plugins:**
- **Related agents:**
- **Shared workspace or files:**
- **Expected operating hours:**
- **Backup / export reference:**
- **Last health check:**
- **Known limitations:**
- **Next review date:**

## Status Definitions

Use the status values reported by the installed management CLI. The skill describes:

- **online:** running in a tmux session.
- **offline:** registered but without an active session.
- **hibernated:** state saved and session stopped.

Refresh the inventory after lifecycle or plugin changes. Avoid treating a stale inventory as proof of live status.
