---
name: send-campaign
description: Draft, preview and send or schedule a Hatched Send email campaign to an audience. Use when the user wants to email a list, send a newsletter or announce something to subscribers.
---

Use the hatched-send MCP tools.

1. Call `list_workspaces` first if the user may have more than one workspace, and work in the one they name.
2. Call `get_brand` so the email uses the workspace's logo, colours and fonts.
3. Write the email as MJML, save it with `create_campaign` (or `create_template` to reuse it), then call `preview_email` and show the preview link.
4. Offer `send_test_email` (it only goes to the user's own address).
5. To send or schedule, call `send_campaign` or `schedule_campaign` without a confirmation code first. Show the subject, sender, audience name, recipient count and preview link. Only call again with the code after the user confirms in their own words. Never send on your own initiative.
