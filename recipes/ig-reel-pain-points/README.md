# IG Reel Pain Points

Daily heartbeat recipe for finding pain points from public internet discussion and turning them into Instagram Reel tests.

## Purpose

Help an Instagram account generate daily, testable Reel ideas from current creator, freelancer, solopreneur, and small-business pain points.

## Recommended Automation Type

`heartbeat`

Reason: the user wants a daily digest even when the local machine may be asleep. The heartbeat returns the digest to a Codex thread. The user can later sync valuable outputs into the AI work-log vault with `automation-vault-sync`.

## Recommended Schedule

Daily at 08:00 local time.

```text
FREQ=DAILY;BYHOUR=8;BYMINUTE=0;BYSECOND=0
```

## Inputs

- Public web discussion.
- Public social/community topics.
- AI tool updates and public product listings.
- Account-specific audience and format constraints.

## Output

The heartbeat should produce:

1. Top 5 pain points.
2. 10 Reel test ideas.
3. 3 priority shoots.
4. A reusable prompt.
5. Public sources.
6. A markdown-ready `Vault Sync Block`.

## Vault Sync

Target path:

```text
<work-log-root>/inbox/YYYY/MM/DD/automations/ai-reel/
```

Sync command:

```text
Use $automation-vault-sync to sync the latest Vault Sync Block into my AI work-log vault.
```

## Security

Do not commit the live Codex automation file. It may include a private `target_thread_id`.

Use [codex-automation.example.toml](codex-automation.example.toml) only as a redacted reference.
