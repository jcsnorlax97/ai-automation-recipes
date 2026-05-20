# Security

This repo is designed for shareable automation recipes only.

## Never Commit

- API keys, access tokens, refresh tokens, passwords, cookies, SSH keys, or private keys.
- Live `~/.codex/automations/*/automation.toml` files.
- `target_thread_id` values.
- Private workspace paths that reveal sensitive clients, employers, or personal data.
- Generated automation output, work-log inbox files, daily notes, raw transcripts, or private Obsidian vault content.
- Customer data, private URLs, confidential meeting notes, or internal work artifacts.

## Redaction Rules

Use placeholders:

```text
<account-handle>
<automation-id>
<project-name>
<work-log-root>
<thread-id-redacted>
<private-path-redacted>
```

If a value is required for a real local install, document where it should be inserted instead of committing the value.

## Recipe Review Checklist

Before committing a recipe:

1. Search for `target_thread_id`, `token`, `secret`, `cookie`, `password`, and `PRIVATE`.
2. Confirm examples use placeholders for paths and ids.
3. Confirm generated output is not included.
4. Confirm the `Vault Sync Block` writes to `automations/<automation-id>/`, not `conversations/`.
5. Confirm the recipe can be understood without exposing local runtime state.
