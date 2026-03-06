# sirrlock/claude — Claude Development Guide

## Purpose

Claude.ai Cowork plugin for Sirr. Two use cases:
- **Share mode**: anonymous burn-after-read link via `sirrlock.com/api/public/secret`. No account needed.
- **Vault mode**: named secrets via `sirr.sirrlock.com`. Requires `SIRR_TOKEN` from sirrlock.com/dashboard.

## Structure

```
plugin.json        ← Cowork plugin manifest
.mcp.json          ← wires @sirrlock/mcp (npx), SIRR_SERVER=sirr.sirrlock.com, SIRR_TOKEN optional
skills/
  share.md         ← instructions for anonymous share flow
  vault.md         ← instructions for named vault flow (with onboarding if no token)
commands/
  share.md         ← /share entry point
```

## MCP dependency

Uses `@sirrlock/mcp` (published to npm). The `share_secret` tool was added specifically for this plugin — it calls `sirrlock.com/api/public/secret` with no auth required.

## Sequencing

1. Share mode — done
2. Vault mode — stub (onboarding to sirrlock.com/dashboard)
3. After sirrlock.com onboarding is improved — complete vault mode wiring
