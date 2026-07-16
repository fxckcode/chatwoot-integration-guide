---
name: chatwoot-skills
description: >-
  Comprehensive skill for integrating Chatwoot — the open-source customer support platform — into any system. Covers setup, channels, live chat widget, features, automation, Captain AI, migrations, and best practices.
license: MIT
metadata:
  author: fxckcode
  version: "1.0"
---

# Chatwoot Integration Guide

Use this skill when the user wants to integrate, configure, or extend Chatwoot in any system. It covers the complete platform: cloud-hosted, self-hosted, and enterprise editions.

## Quick Reference

| Topic | Key Docs |
|-------|----------|
| **First setup** | `articles/getting-started-chatwoot-101.md`, `articles/create-your-chatwoot-account.md` |
| **Channels** | `articles/how-to-setup-a-whats_app-channel.md`, `articles/adding-inboxes.md` |
| **Live chat** | `articles/website-live-chat-settings-explained.md`, `articles/how-to-install-live_chat-on-a-next-js-app.md` |
| **Captain AI** | `articles/captain-_-introduction.md`, `articles/creating-an-assistant-with-captain.md` |
| **Webhooks** | `articles/how-to-use-webhooks.md` |
| **API** | `articles/how-to-create-an-api-channel-inbox.md` |
| **Migrations** | `articles/how-to-migrate-from-zendesk-to-chatwoot.md` |

## Table of Contents

- [Quick Reference](#quick-reference)
- [Platform Overview](#platform-overview)
- [Setup & Configuration](#setup--configuration)
- [Channels (Inboxes)](#channels-inboxes)
- [Website Live Chat Widget](#website-live-chat-widget)
- [Core Features](#core-features)
- [Advanced Features](#advanced-features)
- [Apps & Integrations](#apps--integrations)
- [Captain AI](#captain-ai)
- [Reports & Analytics](#reports--analytics)
- [Help Center](#help-center)
- [Best Practices](#best-practices)
- [Self-Hosted Deployment](#self-hosted-deployment)
- [Migrations](#migrations)
- [Troubleshooting](#troubleshooting)
- [API Reference](#api-reference)

## Platform Overview

Chatwoot is an open-source customer support platform (alternative to Intercom & Zendesk) available in:
- **Cloud** — SaaS at chatwoot.com
- **Self-hosted** — Open-source community edition
- **Enterprise** — Self-hosted with enterprise features

### Key Concepts

| Concept | Description |
|---------|-------------|
| **Account** | Top-level organization. Each account has its own settings, users, and data |
| **Inbox** | A channel connection (WhatsApp, Email, Website, etc.). Conversations live in inboxes |
| **Conversation** | A thread between a customer and agents within an inbox |
| **Contact** | A customer profile with conversation history and attributes |
| **Agent** | A team member who handles conversations |
| **Team** | A group of agents for routing and filtering |
| **Label** | Tags for organizing conversations |
| **Custom Attribute** | Extra data fields on contacts or conversations |
| **Captain** | Chatwoot's built-in AI agent for automated customer support |

See `articles/chatwoot-glossary.md` for the full glossary.

## Setup & Configuration

### Creating an Account

1. Go to https://app.chatwoot.com and sign up
2. Confirm email and set workspace name
3. Complete onboarding wizard (or skip to dashboard)

See `articles/create-your-chatwoot-account.md`.

### Profile & Settings

| Setting | Article |
|---------|---------|
| Personal profile | `articles/customizing-your-personal-profile.md` |
| General settings | `articles/customizing-your-general-settings.md` |
| Notification preferences | `articles/setting-up-notifications.md` |

### Managing Agents

Add agents via Settings → Agent Management:
- Agents get email invitations
- Roles: Agent (default), Administrator (full access)
- See `articles/adding-agents.md`

### Role-Based Permissions

Chatwoot v3.18+ supports granular role-based access control:
- Custom roles with per-feature permissions
- Manage team access with flexible permissions
- See `articles/manage-team-access-control-with-flexible-role_based-permissions.md`

### Teams

Create teams in Settings → Teams:
- Route conversations to specific teams
- Filter by team in reports
- See `articles/adding-teams.md`

### Labels

Create and manage labels in Settings → Labels:
- Color-coded categories
- Apply to conversations and contacts
- Filter conversations by label
- See `articles/how-to-add-labels.md`

### Custom Attributes

Define custom fields for contacts and conversations:
- Text, number, date, dropdown, checkbox types
- Use in automations, campaigns, and API
- See `articles/how-to-create-and-use-custom-attributes.md`

### SAML SSO

Enterprise feature:
- Configure SAML in Settings → Login & Authentication
- Supports Okta, Azure AD, Google Workspace, and custom IdPs
- See `articles/setting-up-saml.md`

## Channels (Inboxes)

An **inbox** is a channel connection. Each inbox type has specific setup steps.

### WhatsApp

| Method | Best for | Article |
|--------|----------|---------|
| **Meta Embedded Signup** | Easy, official | `articles/how-to-use-whatsapp-embedded-signup.md` |
| **Manual (Meta)** | Existing Meta setup | `articles/how-to-setup-a-whats_app-channel-manual-flow.md` |
| **Twilio** | Twilio customers | `articles/how-to-set-up-a-whats_app-channel-with-twilio.md` |

Key considerations:
- WhatsApp templates need approval from Meta
- Message templates for proactive outreach
- See `articles/whatsapp-templates.md` and `articles/twilio-content-templates.md`
- CSAT surveys work on WhatsApp: `articles/whats_app-csat-surveys-in-chatwoot.md`
- Common issues: `articles/common-whats_app-issues-and-how-to-fix-them.md`
- Brazil/Argentina number quirks: `articles/inconsistencies-for-whats_app-numbers-in-brazil-mexico-and-argentina.md`
- Migrate embedded signup to manual: `articles/migrate-a-whats_app-embedded-signup-inbox-to-manual-setup.md`

### Facebook & Instagram

| Channel | Setup Guide |
|---------|-------------|
| **Facebook Page** | `articles/how-to-setup-a-facebook-channel.md` |
| **Instagram (via Facebook)** | `articles/how-to-setup-an-instagram-channel.md` (Legacy) |
| **Instagram (direct login)** | `articles/how-to-setup-an-instagram-channel-via-instagram-login.md` |
| **Human Agent Tag** | `articles/what-is-human-agent-tag-in-instagram-messenger-channel.md` |

### Email Channel

Connect any IMAP/SMTP email:
```
IMAP: imap.example.com:993 (SSL)
SMTP: smtp.example.com:587 (TLS)
```
See `articles/how-to-setup-an-email-channel.md`.

### SMS (Twilio)

- Uses Twilio messaging service
- Supports short codes and long codes
- See `articles/how-to-setup-an-sms-channel.md`

### Other Channels

| Channel | Article |
|---------|---------|
| Twitter | `articles/how-to-setup-a-twitter-channel.md` |
| Telegram | `articles/how-to-setup-a-telegram-channel.md` |
| Line | `articles/how-to-setup-a-line-channel.md` |
| TikTok | `articles/how-to-setup-a-tik_tok-channel.md` |
| API Inbox | `articles/how-to-create-an-api-channel-inbox.md` |

### Voice Channels

| Provider | Article |
|----------|---------|
| Twilio Voice | `articles/connecting-twilio-voice-channel.md` |
| WhatsApp Voice | `articles/connecting-whats_app-voice-channel.md` |
| Voice Overview | `articles/voice-calling-in-chatwoot.md` |

## Website Live Chat Widget

### Installation

The Chatwoot live chat widget can be installed on any website or app:

```
<script>
  window.chatwootSettings = {
    hideMessageBubble: false,
    position: 'right',  // 'left' or 'right'
    locale: 'en',
    type: 'standard'    // 'standard' or 'expanded_bubble'
  };
  (function(d,t) {
    var g=d.createElement(t),s=d.getElementsByTagName(t)[0];
    g.src='https://app.chatwoot.com/pwa/plugin.js';
    g.defer=1;g.async=1;s.parentNode.insertBefore(g,s);
  })(document,'script');
</script>
```

See `articles/website-live-chat-settings-explained.md` for all settings.

### Platform Guides

| Platform | Article |
|----------|---------|
| Next.js | `articles/how-to-install-live_chat-on-a-next-js-app.md` |
| Vue.js | `articles/how-to-install-live_chat-on-a-vue-js-app.md` |
| React Native | `articles/how-to-install-live_chat-on-a-react-native-app.md` |
| WordPress | `articles/how-to-install-live-chat-on-a-word_press-website.md` |
| Docusaurus | `articles/how-to-install-live-chat-on-a-docusaurus-website.md` |
| Gatsby | `articles/how-to-install-live-chat-on-a-gatsby-website.md` |
| Webflow | `articles/how-to-install-live-chat-on-a-webflow-website.md` |
| Google Tag Manager | `articles/how-to-install-live-chat-using-google-tag-manager.md` |
| Vanilla JS | Base script above |

### Advanced Widget Features

| Feature | Article |
|---------|---------|
| Custom user data via SDK | `articles/how-to-send-additional-user-information-to-chatwoot-using-sdk.md` |
| Identity validation | `articles/how-to-enable-identity-validation-in-chatwoot.md` |
| Dark mode | `articles/how-to-enable-dark-mode-on-live_chat-widget.md` |
| Continue conversations via email | `articles/how-to-continue-conversations-through-email.md` |
| Contact identity validation | `articles/understanding-contact-identity-and-identity-validation-in-chatwoot.md` |

### Identity Validation (HMAC)

To prevent impersonation, enable HMAC-based identity validation:

```javascript
// Server-side: generate HMAC
const crypto = require('crypto');
const hmac = crypto.createHmac('sha256', CHATWOOT_SECRET_KEY);
hmac.update(contact_identifier);
const identifierHash = hmac.digest('hex');

// Client-side: pass to widget
window.chatwootSettings = {
  identifier: user.email,
  identifierHash: identifierHash,  // from server
  user: {
    name: user.name,
    email: user.email,
    avatar_url: user.avatar
  }
};
```

See `articles/how-to-enable-identity-validation-in-chatwoot.md`.

## Core Features

### Conversations

| Feature | Article |
|---------|---------|
| Conversation filters | `articles/how-to-use-conversation-filters.md` |
| Priority assignment | `articles/how-to-assign-a-priority.md` |
| Sorting | `articles/how-does-sorting-work.md` |
| CSAT surveys | `articles/how-to-enable-csat-surveys.md` |
| WhatsApp CSAT | `articles/whats_app-csat-surveys-in-chatwoot.md` |
| CSAT review notes | `articles/review-notes-for-csat.md` |
| Agent collision prevention | `articles/preventing-agent-collision.md` |
| Business hours & auto-responder | `articles/business-hours-and-auto_responder.md` |
| Required conversation attributes | `articles/required-conversation-attributes.md` |

### Canned Responses (Saved Replies)

Create reusable message templates:
1. Settings → Canned Responses → Add
2. Set a shortcut key (e.g., `!greeting`)
3. Type `!greeting` in conversation to expand

See `articles/how-to-create-saved-reply-templates-with-canned-responses.md`.

### Pre-Chat Forms

Customize the form customers see before starting a chat:
- Add custom fields
- Make fields required or optional
- See `articles/how-to-use-pre_chat-forms.md`

### Interactive Messages

Send structured messages with buttons and actions:
- Cards with images, titles, and descriptions
- Action buttons (link, postback)
- See `articles/how-to-use-interactive-messages.md`

### Macros

Pre-defined actions that can be applied to conversations:
- Assign, add label, send message, change status
- Apply manually or via automation rules
- See `articles/how-to-use-macros.md`

### Omnichannel Message Signature

Set different signatures per channel:
- HTML-supported signatures
- Channel-specific: one for email, another for WhatsApp
- See `articles/how-to-use-the-omnichannel-message-signature.md`

### Mobile Apps

| Platform | Article |
|----------|---------|
| Android | `articles/mobile-app-for-android.md` |
| iOS | `articles/mobile-app-for-i_os.md` |

### Agent Capacity

Limit how many concurrent conversations an agent can handle:
- Settings → Agent Capacity
- Prevents agent overload
- See `articles/agent-capacity.md`

## Advanced Features

### Automation

Create if-this-then-that rules for conversations:

```yaml
# Example automation rule
trigger: conversation_created
conditions:
  - attribute: inbox_id
    operator: equal_to
    value: "1"
actions:
  - action: send_email_transcript
  - action: add_label
    value: "auto-responded"
```

Conditions available:
- Conversation attributes (status, priority, inbox, etc.)
- Message content
- Contact attributes
- Timing (business hours, etc.)

Actions available:
- Change status/priority/assignee
- Add/remove labels
- Send message/email transcript
- Mute conversation

See `articles/how-to-use-automation.md`.

### Assignment Rules (Assignment V2)

Automatic conversation routing:
- Round-robin: evenly distribute across agents
- Capacity-based: assign based on agent workload
- Team-based: route to specific teams
- Custom rules: match conditions to assignee

See `articles/chatwoot-assignment-v2.md` and `articles/assigning-conversations-in-a-round_robin-fashion.md`.

### SLA (Service Level Agreements)

Define and enforce response/resolution times:
1. Settings → SLA → Add policy
2. Set FRIT (First Response In Time) and NRT (Next Response Time)
3. Configure breach actions (escalate, notify, mark priority)

Reports available: `articles/how-to-read-the-sla-reports.md`
Setup: `articles/service-level-agreemtns.md`

### Campaigns

Send targeted messages to contacts:

| Type | Use Case |
|------|----------|
| **One-off** | Broadcast to segment |
| **Ongoing** | Automated drip campaigns |
| **Widget campaigns** | In-app messages on websites |

Wildcard URL matching: `articles/wildcard-url-support-in-website-live_chat-campaigns.md`
See `articles/how-to-use-campaigns.md`.

### Webhooks

Receive real-time events from Chatwoot:

```bash
# Configure webhook URL in Settings → Integrations → Webhook
# Events: conversation_created, message_created, contact_created, etc.
# Payload format: JSON with event type, conversation data, contact data
```

See `articles/how-to-use-webhooks.md`.

### Agent Bots

Automate responses with bot agents:
- Built-in bots or custom webhook bots
- Handle common queries before human escalation
- See `articles/how-to-use-agent-bots.md`

### Audit Logs

Track all changes in the account:
- Who did what and when
- Settings changes, agent actions, system events
- See `articles/how-to-use-audit-logs.md`

### WebSocket Connection

Real-time events via WebSocket:
```javascript
const socket = new WebSocket('wss://app.chatwoot.com/cable');
// Subscribe to conversation pushes
// Receive real-time message and status updates
```
See `articles/how-to-setup-a-web_socket-connection.md`.

### Dashboard Apps

Embed third-party tools in the Chatwoot sidebar:
- Custom React/Vue apps
- Receive conversation context
- Execute actions via API
- See `articles/how-to-use-dashboard-apps.md`

### Template Variables

Use dynamic variables in messages and responses:
```
Hello {{contact.name}},
Your ticket {{conversation.display_id}} has been updated.
Status: {{conversation.status}}
```
See `articles/template-variables.md`.

## Apps & Integrations

### Slack Integration

Reply to Chatwoot conversations directly from Slack:
1. Settings → Integrations → Slack
2. Authorize Slack workspace
3. Choose notification preferences
4. Reply from Slack threaded messages

See `articles/how-to-answer-conversations-from-slack.md`.

### Dialogflow Chatbot

Connect Google Dialogflow for NLU-powered bots:
1. Create Dialogflow agent
2. Export as ZIP, upload to Chatwoot
3. Connect to inbox as Agent Bot
4. Intents → bot responses automatically

See `articles/how-to-integrate-your-dialogflow-chatbot-with-chatwoot.md`.

### OpenAI Integration

AI-powered features:
- Suggest replies based on conversation context
- Summarize conversations
- Translate messages
- See `articles/openai.md`

### Google Translate

Auto-translate messages within conversations:
- Enable in Settings → Integrations
- Translate incoming/outgoing messages
- See `articles/how-to-translate-your-messages-with-google-translate.md`

### Dyte Video Calls

Enable video calls in conversations:
1. Settings → Integrations → Dyte
2. Add Dyte API key
3. Agents can start video calls from conversation

See `articles/how-to-enable-video-calls-with-dyte-integration.md`.

### Linear Integration

Track issues and features from conversations:
- Link Linear issues to conversations
- Create issues from Chatwoot
- See `articles/how-to-track-issues-and-features-with-linear-integration.md`

### Cloudflare Realtime Kit

Alternative video call provider:
- Enable video calls with Cloudflare
- See `articles/how-to-enable-video-calls-with-cloudflare-realtime_kit.md`

### Dashboard Apps (Custom)

Build custom dashboard apps:
- Embed in the conversation sidebar
- React/Vue components
- Receive conversation context via postMessage
- Execute Chatwoot API calls

See `articles/how-to-use-dashboard-apps.md`.

## Captain AI

Captain is Chatwoot's built-in AI assistant for automated customer support.

### Setup

1. Enable Captain in Settings → Captain
2. Create an assistant with a personality/prompt
3. Connect to an inbox
4. Configure auto-resolution settings

See `articles/captain-_-introduction.md` and `articles/creating-an-assistant-with-captain.md`.

### Knowledge Base (FAQ)

Upload documents and FAQs for Captain to reference:
- Supported formats: PDF, DOCX, TXT, MD
- Create Q&A pairs manually
- See `articles/creating-an-faq-with-captain.md`
- See `articles/creating-a-document-in-captain.md`

### Memories

Captain can remember facts about contacts across conversations:
- Automatically extracted from chat history
- Manually addable via the Memories panel
- See `articles/how-to-use-captain-memories.md`

### Copilot

Agents can use Captain as a copilot:
- Suggest replies
- Summarize conversations
- Research information from connected sources
- See `articles/how-to-use-captain-copilot.md`

### Custom Tools

Extend Captain with API-connected tools:
- Define tool with name, description, and API schema
- Captain calls the tool when relevant
- See `articles/v2-_-how-to-set-up-custom-tools-for-captain.md`

### Self-Hosted Captain

Enable Captain on self-hosted installations:
- Requires OpenAI API key or Ollama endpoint
- Configure in environment variables
- See `articles/how-to-enable-captain-on-self_hosted-installations.md`

### AI Credits

- Each AI operation (message, FAQ match, tool call) consumes credits
- Purchase credits or subscribe to a plan
- See `articles/how-ai-credits-work-in-captain.md`

### Crawling Your Website

Captain can crawl your website for answers:
- Update robots.txt to allow Chatwoot Assistant
- See `articles/updating-robots-txt-to-allow-chatwoot-assistant-to-crawl-your-website.md`

## Reports & Analytics

| Report | Article |
|--------|---------|
| Overview / Realtime | `articles/how-to-read-overview-reports-realtime.md` |
| CSAT Reports | `articles/how-to-read-csat-reports.md` |
| Conversations Report | `articles/how-to-read-conversations-report.md` |
| SLA Reports | `articles/how-to-read-sla-reports.md` |
| Agent / Label / Inbox / Team | `articles/reading-conversations-agents-labels-inbox-and-team-reports.md` |
| Bot Reports | `articles/how-to-read-the-bot-reports.md` |

## Help Center

Set up a knowledge base/help center within Chatwoot:
1. Settings → Help Center → Add portal
2. Create categories and articles
3. Customize with branding
4. Publish to custom domain

See `articles/how-to-setup-a-help-center.md`.

### SSL Certificate

For custom help center domains:
- Generate or upload SSL certificate
- See `articles/generate-ssl-certificate.md`

### Embedding Videos

Embed video content in help center articles:
- YouTube, Vimeo, Loom support
- See `articles/embedding-videos-in-help-center.md`

### Embed Help Center in Live Chat

Show help center articles inside the live chat widget:
- Helps customers self-serve before messaging
- See `articles/how-to-embed-your-help-center-articles-in-the-live-chat-widget.md`

## Best Practices

### Round Robin Assignment

Distribute conversations evenly among team members:
- Settings → Assignment → Round Robin
- Prevents agent overload
- See `articles/assigning-conversations-in-a-round_robin-fashion.md`

### Command Bar

Quick actions with Cmd/Ctrl + K:
- Navigate conversations
- Change settings
- Apply macros
- See `articles/working-with-command-bar.md`

### Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `C` | New conversation |
| `Cmd/Ctrl + Enter` | Send message |
| `E` | Toggle email notification |
| `M` | Mute conversation |
| `Cmd/Ctrl + Shift + C` | Toggle dark mode |

See `articles/working-with-keyboard-shortcuts.md`.

### Conversation Folders

Save filtered views as folders:
- Group conversations by status, label, assignee, etc.
- Quick access from sidebar
- See `articles/group-chats-with-filters-save-as-folders.md`

### Contact Segments

Filter and group contacts by attributes:
- Save as custom segments for campaigns
- Target specific user groups
- See `articles/group-your-contacts-using-filters-and-save-them-as-custom-segments.md`
- See `articles/how-to-segment-contacts-in-chatwoot.md`

## Self-Hosted Deployment

### Prerequisites

- Docker & Docker Compose
- Minimum: 2 CPU, 4GB RAM
- Domain with SSL (Caddy/Let's Encrypt)
- PostgreSQL (bundled or external)
- Redis (bundled or external)

### Quick Deploy

```bash
git clone https://github.com/chatwoot/chatwoot.git
cd chatwoot
cp .env.example .env
# Edit .env with your settings
docker compose up -d
```

### Enterprise Edition

For self-hosted with enterprise features:
- Purchase license at chatwoot.com/pricing
- Configure license key in environment
- See `articles/purchasing-a-paid-self_hosted-chatwoot-license-a-step_by_step-guide.md`

See also `articles/enterprise-edition.md`.

### SSL Certificate

See `articles/generate-ssl-certificate.md` for setting up SSL.

## Migrations

### From Zendesk

1. Export Zendesk data (conversations, contacts, articles)
2. Import to Chatwoot via API
3. Recreate inboxes and teams
4. Test and switch DNS

See `articles/how-to-migrate-from-zendesk-to-chatwoot.md`.

### From Freshdesk

See `articles/how-to-migrate-from-freshdesk-to-chatwoot.md`.

### From Intercom

See `articles/how-to-migrate-from-intercom-to-chatwoot.md`.

### From Front

See `articles/how-to-migrate-from-front-to-chatwoot.md`.

### WhatsApp Embedded to Manual

See `articles/migrate-a-whats_app-embedded-signup-inbox-to-manual-setup.md`.

## Troubleshooting

| Problem | Solution |
|---------|----------|
| No notifications | `articles/troubleshooting-why-am-i-not-receiving-notifications.md` |
| Browser push not working | `articles/how-to-enable-push-notifications-in-your-browser.md` |
| WhatsApp number issues (Brazil/AR) | `articles/inconsistencies-for-whats_app-numbers-in-brazil-mexico-and-argentina.md` |
| "Free usage limit exceeded" | `articles/how-to-remove-the-free-usage-limit-exceeded-message-in-chatwoot.md` |
| Need hard reload | `articles/how-to-hard_reload-on-most-browsers.md` |

### Personal Access Token

Generate API tokens:
1. Settings → Profile → Access Token
2. Create token with scoped permissions
3. Use in API calls and custom integrations
See `articles/how-to-find-your-personal-access-token-in-chatwoot.md`.

## API Reference

### Authentication

All API requests require a Personal Access Token or Account Token:

```bash
curl -H "api_access_token: YOUR_TOKEN" \
     https://app.chatwoot.com/api/v1/
```

### Key Endpoints

| Endpoint | Purpose |
|----------|---------|
| `GET /api/v1/accounts/{id}/inboxes` | List inboxes |
| `POST /api/v1/accounts/{id}/inboxes` | Create inbox |
| `GET /api/v1/accounts/{id}/conversations` | List conversations |
| `POST /api/v1/accounts/{id}/conversations` | Create conversation |
| `POST /api/v1/accounts/{id}/conversations/{id}/messages` | Send message |
| `GET /api/v1/accounts/{id}/contacts` | List contacts |
| `POST /api/v1/accounts/{id}/contacts` | Create contact |
| `POST /api/v1/accounts/{id}/contacts/{id}/conversations` | Start conversation for contact |
| `GET /api/v1/accounts/{id}/webhooks` | List webhooks |
| `POST /api/v1/accounts/{id}/webhooks` | Create webhook |

### API Inbox Pattern

For sending messages via API channel:

```bash
# 1. Create an API channel inbox
# 2. Get the inbox ID and API key
# 3. Send messages via the API
curl -X POST https://app.chatwoot.com/api/v1/accounts/{id}/conversations/{id}/messages \
  -H "api_access_token: YOUR_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"content": "Hello from API!", "message_type": "outgoing"}'
```

### Webhook Events

Configure Chatwoot to POST events to your URL:
- `conversation_created`, `conversation_updated`
- `message_created`, `message_updated`
- `contact_created`, `contact_updated`
- Webhook payload includes full conversation/contact data

See `articles/how-to-use-webhooks.md`.

### WebSocket Events

Subscribe to real-time events:
```
wss://app.chatwoot.com/cable
```
Channels:
- `Room::ConversationInboxChannel` — inbox-scoped
- `Room::AccountChannel` — account-wide

See `articles/how-to-setup-a-web_socket-connection.md`.

## Languages & Internationalization

Chatwoot supports 20+ languages. Change in Settings:
- Profile → Language
- See `articles/languages-supported-in-chatwoot.md`

## Cookies

Chatwoot uses minimal cookies:
- Session cookie (authentication)
- Widget cookies (visitor tracking)
- See `articles/which-cookies-are-used-by-chatwoot.md`
