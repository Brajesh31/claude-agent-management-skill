# AI Maestro Agent Management Skill

A Claude Code skill for managing local AI agent lifecycles and plugins through the AI Maestro command-line workflow. It covers agent creation, inspection, updates, session control, export and import, plugin management, and operational safeguards.

This repository contains the skill instructions plus practical runbooks for planning and executing lifecycle operations safely.

## What It Helps Manage

| Area | Operations |
|---|---|
| Agent discovery | List configured agents and inspect an individual agent |
| Agent lifecycle | Create, update, rename, delete, hibernate, wake, and restart |
| Configuration portability | Export and import agent configurations |
| Plugins | Install, uninstall, and list plugins; add marketplaces |
| Operations | Check state, verify workspaces, preserve backups, and inspect outcomes |

## Prerequisites

The documented commands require:

- AI Maestro and its agent CLI installed and configured locally.
- tmux 3.0 or newer, as required by the skill instructions.
- A workspace path for each agent.
- Appropriate permissions for the requested operation.

The CLI is a separate dependency. Installing this Claude Code skill does not install AI Maestro automatically.

## Installation

Clone this skill into the Claude Code skills directory:

~~~bash
git clone https://github.com/Brajesh31/claude-agent-management-skill.git ~/.claude/skills/agent-management
~~~

The skill instructions describe installing the AI Maestro CLI from the upstream plugin repository:

~~~bash
git clone https://github.com/23blocks-OS/ai-maestro-plugins.git
cd ai-maestro-plugins
./install-agent-cli.sh
~~~

Check the upstream AI Maestro documentation for current installation requirements and command compatibility before running operations.

## Usage

Invoke the skill in Claude Code:

~~~text
/agent-management
~~~

Provide the agent identifier, intended operation, workspace path, and relevant configuration requirements. For destructive or state-changing actions, confirm the target and expected effect before execution.

## Core Command Reference

The commands below are the command patterns documented in SKILL.md. Confirm the installed CLI's current help output before using them because CLI interfaces can change.

### Agent lifecycle

| Command pattern | Purpose |
|---|---|
| aimaestro-agent.sh list | List agents and their status |
| aimaestro-agent.sh show <agent> | Inspect one agent |
| aimaestro-agent.sh create <name> --dir <path> | Create an agent |
| aimaestro-agent.sh update <agent> --task "..." | Update task or tags |
| aimaestro-agent.sh delete <agent> --confirm | Delete an agent |
| aimaestro-agent.sh rename <old> <new> | Rename an agent |
| aimaestro-agent.sh hibernate <agent> | Save state and free resources |
| aimaestro-agent.sh wake <agent> | Resume a hibernated agent |
| aimaestro-agent.sh restart <agent> | Restart an agent session |

### Plugin management

| Command pattern | Purpose |
|---|---|
| aimaestro-agent.sh plugin install <agent> <plugin> | Install a plugin |
| aimaestro-agent.sh plugin uninstall <agent> <plugin> | Remove a plugin |
| aimaestro-agent.sh plugin list <agent> | List installed plugins |
| aimaestro-agent.sh plugin marketplace add <agent> <source> | Add a marketplace |

### Export and import

| Command pattern | Purpose |
|---|---|
| aimaestro-agent.sh export <agent> | Export an agent configuration |
| aimaestro-agent.sh import <file> | Import an agent from a file |

## Recommended Operating Procedure

1. Check that the CLI and tmux are available.
2. List agents and identify the exact target.
3. Inspect the agent and confirm its current status and workspace.
4. Determine whether the requested change is reversible.
5. Export or otherwise back up the configuration before a risky change.
6. Perform one state-changing operation at a time.
7. Inspect the agent again and verify the expected state.
8. Check logs, session output, plugin state, or task results as appropriate.
9. Record the change and any follow-up action.

## Status Reference

| Status | Meaning in the skill instructions |
|---|---|
| online | Running in a tmux session |
| offline | Registered but no active session |
| hibernated | State saved and session stopped |

Do not assume that a process being present means the agent is healthy. Confirm that it can perform its intended task and that its workspace and tools are available.

## Included Resources

- [Agent lifecycle runbook](resources/lifecycle-runbook.md): safe preflight, operation, verification, and recovery sequence.
- [Agent inventory template](resources/agent-inventory-template.md): record identifiers, workspaces, ownership, status, and operational notes.
- [Change safety checklist](resources/change-safety-checklist.md): use before deletion, restart, configuration changes, and plugin operations.

## Operational Safety

- Confirm the exact agent identifier before making changes.
- Verify the workspace path before creating or waking an agent.
- Export important configurations before risky changes.
- Avoid multiple agents writing to the same files without coordination.
- Review plugin source and permissions before installation.
- Require explicit confirmation for destructive operations.
- Check the resulting state instead of assuming the command succeeded.
- Keep credentials and secrets out of exported templates and logs.

## Repository Structure

~~~text
claude-agent-management-skill/
├── SKILL.md
├── README.md
├── LICENSE
└── resources/
    ├── agent-inventory-template.md
    ├── change-safety-checklist.md
    └── lifecycle-runbook.md
~~~

## Upstream Project

- [AI Maestro](https://github.com/23blocks-OS/ai-maestro)
- [AI Maestro plugins and CLI installer](https://github.com/23blocks-OS/ai-maestro-plugins)

## License

Released under the MIT License. Copyright (c) 2026 Brajesh Kumar. See the root LICENSE file for the complete terms.
