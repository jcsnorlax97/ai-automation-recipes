# Repo Agent Guide

## Communication

- Use traditional Chinese to reply unless the user explicitly asks for another language.
- Prefer concise, direct engineering communication.

## Personal AI OS Roadmap

Before planning work related to automation recipes, Codex automations, heartbeat
or cron recipe design, Vault Sync Blocks, work-log integration, or cross-system
roadmap decisions, read:

```text
/Users/jcsnorlax97/Documents/a-ai-codex/ai-ops-ecosystem-spec/spec/ROADMAP.md
```

Use that roadmap as the current source of truth for how automation recipes fit
into the Personal AI Operating System.

## Repo Boundary

- This repo owns shareable, redacted automation recipes and output contracts.
- Do not commit live automation configs, target thread ids, private local paths,
  generated automation outputs, credentials, cookies, tokens, or private vault
  content.
- Automation digests saved for review belong in the private work-log vault, not
  this repo.

## Safety

- 禁止批量刪除文件或目錄。
- 不要使用 `del /s`、`rd /s`、`rmdir /s`、`Remove-Item -Recurse`、`rm -rf`。
- 如需刪除文件，只能一次刪除一個明確路徑的文件。
- 如果需要批量刪除，停止並請用戶手動處理。
