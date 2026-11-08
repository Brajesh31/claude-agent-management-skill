# claude-agent-management-skill

A Claude Code skill for managing local AI agent lifecycles and plugins through a command-line workflow.

## Overview

This skill focuses on operational management of multiple agents. It covers creating agents, inspecting status, updating configuration, restarting or hibernating sessions, importing and exporting configurations, and managing plugins.

The workflow assumes that the required local agent-management environment has already been installed and configured.

## Main Capabilities

- Create agents with a name, workspace, task, and tags.
- List configured agents.
- Inspect individual agent details and status.
- Update or rename an agent.
- Restart, hibernate, and wake agent sessions.
- Export and import agent configurations.
- Install, remove, and list plugins.
- Check the local environment before performing operations.

## Prerequisites

The commands described by this skill require the AI Maestro CLI and a compatible local environment. The documented workflow also expects tmux 3.0 or newer.

Review the setup and configuration steps in `SKILL.md` before running management commands.

## Installation

```bash
git clone https://github.com/Brajesh31/claude-agent-management-skill.git ~/.claude/skills/agent-management
```

Install and configure the required agent-management CLI separately.

## Usage

Invoke the skill for agent lifecycle tasks:

```text
/agent-management
```

Specify the agent identifier, intended operation, workspace, and any relevant state or configuration requirements.

## Typical Workflow

1. Run the environment diagnostic.
2. List available agents.
3. Inspect the target agent and workspace.
4. Confirm the intended operation.
5. Create or update the agent configuration.
6. Start, restart, hibernate, or wake the session as required.
7. Monitor status and inspect output.
8. Export important configurations before risky changes.

## Operational Safety

- Confirm the target agent before destructive actions.
- Verify the workspace path before starting work.
- Avoid running multiple agents against the same files without coordination.
- Preserve configuration before making large changes.
- Monitor resource usage when running many agents.
- Do not assume an agent is healthy merely because its process exists.
- Check logs and task output before reporting completion.

## Repository Contents

- `SKILL.md`: Main agent lifecycle instructions and command guidance.
- `README.md`: Setup assumptions, capabilities, and operational workflow.

## Maintenance

Keep command examples aligned with the installed CLI version. Validate agent status and plugin state after changes, and document any environment-specific configuration needed by the team.
