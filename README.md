# AI Automation Recipes

Shareable, redacted recipes for Codex automations and related assistant workflows.

This repo stores reusable automation patterns, prompts, schedules, output contracts, and vault sync templates. It does not store live automation runtime config, private thread ids, generated logs, or personal Obsidian vault content.

## Relationship To The Work-Log System

```text
ai-automation-recipes
  Shareable automation recipes and prompt contracts.

ai-work-log-bootstrap
  Skills, vault structure, templates, and bootstrap scripts.

ai-work-logs
  Private local output vault. Not committed here.
```

## What Belongs Here

```text
recipes/<recipe-id>/README.md
recipes/<recipe-id>/prompt.md
recipes/<recipe-id>/schedule.example.md
recipes/<recipe-id>/vault-sync-block-template.md
recipes/<recipe-id>/codex-automation.example.toml
templates/
spec/
```

Good content:

- Redacted automation prompts.
- Example schedules.
- Output schemas.
- `Vault Sync Block` templates.
- Security notes and install guidance.

Do not commit:

- `~/.codex/automations/*/automation.toml` copied directly from a machine.
- `target_thread_id`, private workspace paths, account secrets, cookies, tokens, or private URLs.
- Generated automation output.
- `ai-work-logs/`, `inbox/`, or `generated/`.

## Current Recipes

- [IG Reel Pain Points](recipes/ig-reel-pain-points/README.md): Daily heartbeat digest that finds creator/small-business pain points and turns them into short Instagram Reel tests.

## Usage Pattern

1. Pick a recipe.
2. Copy the prompt and schedule into Codex Automations or a similar scheduler.
3. Replace placeholders such as `<account-handle>`, `<project>`, and `<automation-id>`.
4. Keep live runtime values private.
5. If the recipe outputs a `Vault Sync Block`, save it with `automation-vault-sync` into `ai-work-logs`.

## Security

Read [SECURITY.md](SECURITY.md) before publishing a recipe or copying an automation from a local machine.
