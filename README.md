# Sirr — Claude Plugin

A [Claude.ai Cowork](https://claude.ai) plugin for secure secret sharing and ephemeral vaults.

## What it does

**Share mode** — share a password, token, or sensitive value via a burn-after-read link. No account needed.

> "Share this password with John" → Claude generates a link that disappears after one click.

**Vault mode** — store a named secret and recall it later in your session.

> "Remember ZOOM_PASSWORD=hunter2" → "What was ZOOM_PASSWORD?" → used and gone.

## Install

1. Open Claude.ai → Plugins → Browse
2. Search **Sirr**
3. Install

Or install from this repo directly in Claude Code.

## Configuration

Share mode works with zero setup.

Vault mode requires a `SIRR_TOKEN` — get one at [sirrlock.com/dashboard](https://sirrlock.com/dashboard).

## Self-hosting

Point `SIRR_SERVER` in `.mcp.json` at your own [sirrd](https://github.com/sirrlock/sirr) instance.
