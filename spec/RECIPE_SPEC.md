# Automation Recipe Spec

This spec defines the structure for shareable automation recipes.

## Folder Layout

```text
recipes/<recipe-id>/
  README.md
  prompt.md
  schedule.example.md
  vault-sync-block-template.md
  codex-automation.example.toml
```

## Required Fields

Each recipe README should include:

- Purpose.
- Target audience or use case.
- Recommended automation type: `heartbeat`, `cron-local`, or `cron-worktree`.
- Recommended schedule.
- Inputs.
- Output format.
- Vault sync behavior.
- Security notes.

## Prompt Contract

`prompt.md` should be the clean automation prompt with placeholders. It must not contain private thread ids, local absolute paths, or generated outputs.

## Schedule Contract

`schedule.example.md` should describe the schedule in human terms and include an example RRULE if useful.

Do not claim a scheduler will catch up missed local runs unless the runtime guarantees that behavior.

## Vault Sync Contract

Recipes that produce durable notes should emit a markdown-ready `Vault Sync Block` with:

```yaml
---
status: inbox
source:
project:
automation_id:
topic:
candidate_tags:
  - work/log
  - automation/codex
needs_review: true
---
```

The target path is:

```text
<work-log-root>/inbox/YYYY/MM/DD/automations/<automation-id>/YYYY-MM-DD-digest.md
```

Use managed markers when the block may be updated:

```markdown
<!-- automation-vault-sync:start -->
...
<!-- automation-vault-sync:end -->
```

## Example TOML Contract

`codex-automation.example.toml` is documentation, not a live config.

It may include:

- `id`
- `kind`
- `name`
- `prompt`
- `status`
- `rrule`

It must not include:

- `target_thread_id`
- real local paths
- secrets
- generated outputs
