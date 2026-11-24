---
name: transactional-email-setup
description: Set up the Hatched Send transactional email API in a developer's project (API key, SDK, sending domain, webhooks). Use when the user says connect my project, send email from my app or add email to my code.
---

Use the hatched-send MCP tools.

1. Call `create_api_key` with mode `test` while building. Test sends are logged but never delivered.
2. If you can edit the project, write the key to `.env.local` as `HATCHED_SEND_API_KEY` and make sure that file is git-ignored. Never print the key in chat.
3. Send with a plain HTTPS call: `POST https://send.hatched.digital/api/v1/email` with the key in an `Authorization: Bearer` header. No SDK is required; see the quickstart for the request body.
4. To send from the user's own domain: `add_sending_domain`, help them publish the DNS records, then `verify_sending_domain`.
5. `register_webhook` returns a signing secret once. Store it like the key.

Quickstart: https://send.hatched.digital/docs/quickstart
