# Remembering and Recalling Named Secrets

The vault lets users store a value under a name and retrieve it later in the same session.

## If SIRR_TOKEN is configured

Use the standard MCP tools:
- Store: `push_secret(key, value)` — e.g. `push_secret("ZOOM_PASS", "hunter2")`
- Recall: `get_secret(key)` — e.g. `get_secret("ZOOM_PASS")`
- After recalling, do NOT repeat or store the value beyond its immediate use.

## If SIRR_TOKEN is NOT configured (empty or missing)

Walk the user through setup:

1. Go to **sirrlock.com/dashboard**
2. Open **API Keys** → **Create Key**
3. Copy the key
4. Paste it into the `SIRR_TOKEN` field in the Sirr MCP config and restart Claude

Then try the vault command again.

## Trigger phrases

Use this skill when the user says things like:
- "remember MY_TOKEN=abc123"
- "store this as ZOOM_PASSWORD"
- "what was MY_TOKEN?"
- "recall DEPLOY_KEY"
