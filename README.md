# claude-agent-management-skill

A Claude Code skill for managing local AI agent lifecycles and plugins through a command-line workflow.

## Overview

This skill covers creating agents, inspecting status, updating configuration, restarting or hibernating sessions, importing and exporting configurations, and managing plugins.

## Main Capabilities

- Create agents with a name, workspace, task, and tags.
- List configured agents and inspect individual details.
- Update or rename agents.
- Restart, hibernate, and wake agent sessions.
- Export and import agent configurations.
- Install, remove, and list plugins.
- Check the local environment before performing operations.

## Prerequisites

The documented workflow requires the AI Maestro CLI and a compatible local environment. It also expects tmux 3.0 or newer. Review setup requirements in `SKILL.md` before running management commands.

## Installation

```bash
git clone https://github.com/Brajesh31/claude-agent-management-skill.git ~/.claude/skills/agent-management
```

Install and configure the required agent-management CLI separately.

## Typical Workflow

1. Run the environment diagnostic.
2. List available agents.
3. Inspect the target agent and workspace.
4. Confirm the intended operation.
5. Create or update the agent configuration.
6. Start, restart, hibernate, or wake the session.
7. Monitor status and inspect output.
8. Export important configurations before risky changes.

## Operational Safety

- Confirm the target agent before destructive actions.
- Verify workspace paths before starting work.
- Avoid running multiple agents against the same files without coordination.
- Preserve configuration before major changes.
- Monitor resource usage when running many agents.
- Check logs and task output before reporting completion.

## Repository Contents

- `SKILL.md`: Main agent lifecycle instructions and command guidance.
- `README.md`: Setup assumptions, capabilities, and operational workflow.

## Creator and maintainer

Created and maintained by **Brajesh Kumar**.
