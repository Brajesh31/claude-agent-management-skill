# Agent Management Skill

A Claude skill for managing the lifecycle of AI agents through the AI Maestro command-line interface. It covers common operational tasks such as creating agents, inspecting their status, updating configuration, hibernating and waking sessions, and managing plugins.

## What This Skill Covers

- Creating agents with a name, workspace directory, task, and tags.
- Listing agents and inspecting individual agent details.
- Updating, renaming, restarting, hibernating, and waking agents.
- Exporting and importing agent configurations.
- Installing, removing, and listing agent plugins.

## Repository Structure

- `SKILL.md`: Skill instructions, prerequisites, command reference, examples, and agent status descriptions.
- `LICENSE`: MIT License for this repository.

## Prerequisites

The instructions expect AI Maestro to be available locally, along with tmux 3.0 or newer. The skill also describes installing the CLI scripts from the AI Maestro plugins repository. Review the prerequisite steps in `SKILL.md` before running commands.

## Typical Workflow

1. Install and configure the AI Maestro CLI.
2. List existing agents and inspect the target workspace.
3. Create or update an agent with a clear task and working directory.
4. Use status commands to monitor whether agents are online, offline, or hibernated.
5. Hibernate inactive agents to release resources, then wake them when work resumes.
6. Export important configurations before making risky changes.

## Usage

Place this repository's skill in a Claude-compatible skills directory and invoke it for agent lifecycle or plugin-management tasks. Commands shown in the skill are intended to be executed in an environment where AI Maestro is installed and configured.

## License

Released under the MIT License. See [LICENSE](LICENSE) for details.
