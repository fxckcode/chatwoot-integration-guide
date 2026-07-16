---
name: chatwoot-api
description: Use Chatwoot REST API, webhooks, and WebSocket for custom integrations. Use when building custom workflows, automating Chatwoot programmatically, or integrating with external systems via API.
---

# Chatwoot API

Integrate with Chatwoot via REST API, webhooks, and WebSocket.

## Authentication

Use a Personal Access Token or Account Token:

```bash
curl -H "api_access_token: YOUR_TOKEN" \
     https://app.chatwoot.com/api/v1/
```

Generate tokens: **Settings → Profile → Access Token**
See `articles/how-to/how-to-find-your-personal-access-token-in-chatwoot.md`.

## Key Endpoints

| Endpoint | Purpose |
|----------|---------|
| `GET /api/v1/accounts/{id}/inboxes` | List inboxes |
| `POST /api/v1/accounts/{id}/inboxes` | Create inbox |
| `GET /api/v1/accounts/{id}/conversations` | List conversations |
| `POST /api/v1/accounts/{id}/conversations` | Create conversation |
| `POST /api/v1/accounts/{id}/conversations/{id}/messages` | Send message |
| `GET /api/v1/accounts/{id}/contacts` | List contacts |
| `POST /api/v1/accounts/{id}/contacts` | Create contact |
| `GET /api/v1/accounts/{id}/webhooks` | List webhooks |
| `POST /api/v1/accounts/{id}/webhooks` | Create webhook |

Full API reference: `references/self-hosted/api-reference-introduction.md`

## API Inbox Pattern

Send messages via API channel:

```bash
curl -X POST https://app.chatwoot.com/api/v1/accounts/{id}/conversations/{id}/messages \
  -H "api_access_token: YOUR_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"content": "Hello from API!", "message_type": "outgoing"}'
```

See `articles/other-channels/how-to-create-an-api-channel-inbox.md`.

## Webhooks

Configure Chatwoot to POST events to your URL:

```bash
# Settings → Integrations → Webhook
# Events arrive as JSON POST to your webhook URL
```

### Events

- `conversation_created`, `conversation_updated`
- `message_created`, `message_updated`
- `contact_created`, `contact_updated`

See `articles/apps-integrations/how-to-use-webhooks.md`.

## WebSocket

Subscribe to real-time events:

```javascript
const socket = new WebSocket('wss://app.chatwoot.com/cable');
// Channels:
// - Room::ConversationInboxChannel (inbox-scoped)
// - Room::AccountChannel (account-wide)
```

See `articles/advanced-features/how-to-setup-a-web_socket-connection.md`.

## Integrations

| Integration | Article |
|-------------|---------|
| Slack | `articles/apps-integrations/how-to-answer-conversations-from-slack.md` |
| Dialogflow | `articles/apps-integrations/how-to-integrate-your-dialogflow-chatbot-with-chatwoot.md` |
| OpenAI | `articles/apps-integrations/openai.md` |
| Google Translate | `articles/apps-integrations/how-to-translate-your-messages-with-google-translate.md` |
| Dyte Video | `articles/apps-integrations/how-to-enable-video-calls-with-dyte-integration.md` |
| Linear | `articles/apps-integrations/how-to-track-issues-and-features-with-linear-integration.md` |
| Cloudflare Video | `articles/apps-integrations/how-to-enable-video-calls-with-cloudflare-realtime_kit.md` |
