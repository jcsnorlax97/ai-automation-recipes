# Cron Local Recipe Template

## Purpose

Describe what the local cron job should produce and why it needs local filesystem access.

## Recommended Schedule

```text
Daily at a time when the user's machine is normally awake.
```

## Local Runtime Assumptions

- The computer must be awake and able to run the Codex local environment.
- Local filesystem access is required.
- Missed runs should not be assumed to catch up automatically.

## Output Target

```text
<work-log-root>/inbox/YYYY/MM/DD/automations/<automation-id>/
```

## Security

Do not scan parent folders or the user's private/main Obsidian vault.

Do not write outside the configured work-log root unless the user explicitly provides a path.
