# Sharing a Secret

When the user wants to share a password, token, API key, or any sensitive value with someone else:

1. Call `share_secret` with the value.
2. Return the URL to the user in this format:

   > Here's your secure link:
   > **[link]**
   > Send it to whoever needs it. It disappears after they open it once, or after 24 hours.

3. Do NOT repeat, display, or store the original secret value after calling the tool.
4. If the user asks to share multiple things, call `share_secret` once per value and return one link per item.

## Trigger phrases

Use this skill when the user says things like:
- "share this password with John"
- "send this token securely"
- "create a one-time link for this"
- "share this without putting it in Slack"
- "burn after read"
