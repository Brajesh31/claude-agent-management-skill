# Agent Management Change Safety Checklist

Use this checklist before making changes that affect an agent, its workspace, session, or plugins.

## Target and Scope

- [ ] The exact agent identifier has been confirmed.
- [ ] The requested operation is unambiguous.
- [ ] The workspace and related files have been checked.
- [ ] Shared workspace dependencies are understood.
- [ ] Other agents that may be affected have been identified.

## Backup and Reversibility

- [ ] The current configuration has been inspected.
- [ ] A configuration export or backup exists when appropriate.
- [ ] The backup is stored in an approved location.
- [ ] Recovery steps are understood.
- [ ] Secrets are not exposed in backup names, logs, or notes.

## Permissions and Side Effects

- [ ] The operator has permission to make the change.
- [ ] Destructive operations have explicit confirmation.
- [ ] Plugin source and requested permissions have been reviewed.
- [ ] No unrelated agent or workspace will be modified.
- [ ] Active work will not be interrupted unexpectedly.

## Execution

- [ ] The installed CLI version and command syntax are confirmed.
- [ ] One state-changing operation is performed at a time.
- [ ] Command output and errors are captured.
- [ ] The operation is not reported as successful before verification.

## Post-Change Verification

- [ ] The target agent has been inspected again.
- [ ] The expected status or configuration is present.
- [ ] Plugin state is correct, when relevant.
- [ ] Workspace access is intact.
- [ ] A focused smoke test has been completed.
- [ ] Unrelated agents and workspaces remain unaffected.

## Change Record

- **Agent:**
- **Operation:**
- **Reason:**
- **Operator:**
- **Date:**
- **Backup reference:**
- **Verification performed:**
- **Outcome:**
- **Follow-up required:**
