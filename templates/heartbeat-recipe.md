# Heartbeat Recipe Template

## Purpose

Describe what the heartbeat should produce and why it should return to a Codex thread.

## Recommended Schedule

```text
Daily at 08:00 local time
RRULE: FREQ=DAILY;BYHOUR=8;BYMINUTE=0;BYSECOND=0
```

## Prompt

```text
Write the automation prompt here.

Use placeholders for anything private:
- <project-name>
- <account-handle>
- <automation-id>
```

## Output Contract

The heartbeat should reply in the thread and include a `Vault Sync Block` when the output is worth saving.

## Vault Sync Target

```text
<work-log-root>/inbox/YYYY/MM/DD/automations/<automation-id>/
```

## Security

Do not write directly to local files from a heartbeat. Use `automation-vault-sync` when the user returns.
