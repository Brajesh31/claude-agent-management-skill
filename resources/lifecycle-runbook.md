# Agent Lifecycle Runbook

Use this runbook for routine AI Maestro agent operations. Confirm the CLI's current command help and the installed version before execution.

## 1. Preflight

- [ ] Confirm AI Maestro is installed and available.
- [ ] Confirm tmux 3.0 or newer is available.
- [ ] Confirm the CLI command resolves in the current shell.
- [ ] Identify the exact agent name.
- [ ] Identify the intended workspace and verify its path.
- [ ] Check whether another agent is using the same workspace.
- [ ] List agents and inspect the target before changing it.
- [ ] Determine whether the operation is destructive or difficult to reverse.

## 2. Create an Agent

1. Choose a unique, descriptive agent name.
2. Verify the intended workspace exists or is ready to be created.
3. Define a concise task and only the required tags.
4. Confirm the requested permissions and plugins.
5. Create the agent using the installed CLI's documented syntax.
6. Inspect the new agent and confirm its configuration.
7. Start or wake it only when required.
8. Verify that it can access the intended workspace.

## 3. Update or Rename

1. Inspect the current agent configuration.
2. Record the current task, tags, workspace, and plugin state.
3. Export a backup when the change could be hard to reverse.
4. Apply one change at a time.
5. Inspect the agent again.
6. Confirm the resulting configuration matches the request.
7. Run a small task to verify expected behavior.

## 4. Hibernate, Wake, or Restart

Before hibernating or restarting, check for unfinished work and active processes.

- Confirm the agent identity.
- Confirm whether work is safe to pause.
- Save or export important state when appropriate.
- Perform the requested lifecycle operation.
- Inspect the resulting status.
- When waking or restarting, verify session availability and task readiness.

## 5. Plugins

Before installing or removing a plugin:

- Confirm the target agent.
- Review the plugin source and expected permissions.
- Check compatibility with the installed AI Maestro version.
- Confirm whether the plugin changes agent behavior or available tools.
- Apply the change.
- List installed plugins and verify the resulting state.
- Run a focused smoke test.

## 6. Delete an Agent

Deletion is destructive. Before proceeding:

- [ ] Confirm the exact agent identifier.
- [ ] Confirm deletion is the requested outcome, not hibernation or removal of a plugin.
- [ ] Export configuration or preserve required files.
- [ ] Check for active work and shared workspace dependencies.
- [ ] Confirm the user has approved the deletion.
- [ ] Run the deletion operation with its explicit confirmation mechanism.
- [ ] List agents and confirm the intended target is no longer registered.
- [ ] Verify that unrelated agents and workspaces remain intact.

## 7. Closeout

- Record what changed.
- Record the final agent status.
- Record backup or export locations without exposing secrets.
- Note any failed checks or remaining actions.
- Report only outcomes that were actually verified.
