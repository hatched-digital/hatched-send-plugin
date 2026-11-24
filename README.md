# Hatched Send for AI assistants

Build, preview and send email campaigns, manage audiences and contacts, and wire up a transactional email API, all from Claude, ChatGPT, Cursor, VS Code, Codex and any MCP app.

This repo is the plugin wrapper: it points your assistant at the hosted Hatched Send connector and adds three skills. The service itself is closed source.

- Connector URL: `https://send.hatched.digital/mcp` (OAuth sign-in, you choose workspaces and permissions)
- Setup steps for every app: https://send.hatched.digital/connect
- Docs: https://send.hatched.digital/docs/claude
- Privacy: https://send.hatched.digital/privacy

## Install

**Claude Code**

    /plugin marketplace add hatched-digital/hatched-send-plugin
    /plugin install hatched-send@hatched

**Cursor, Codex and other Agent Plugins clients:** add this repo as a plugin, or add the connector URL directly.

**Claude, ChatGPT, Grok:** add `https://send.hatched.digital/mcp` as a custom connector.

## Safety

Sending and scheduling are always two steps: the assistant shows a preview with subject, sender, audience and recipient count, and nothing is sent until you confirm. Test emails only go to your own address. Disconnect any time under Settings, Connected apps.

## Skills

`send-campaign`, `manage-audiences`, `transactional-email-setup`.

MIT licensed (the wrapper only).
