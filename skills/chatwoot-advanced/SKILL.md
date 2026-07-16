---
name: chatwoot-advanced
description: Configure Chatwoot advanced features — automation rules, webhooks, SLA policies, assignment rules, agent bots, audit logs, dashboard apps, and custom attributes. Use when setting up automation, integrations, or governance features.
---

# Chatwoot Advanced Features

Advanced capabilities for automation, governance, and extensibility.

## Automation Rules

Create if-this-then-that rules for conversations:

```yaml
trigger: conversation_created
conditions:
  - attribute: inbox_id
    operator: equal_to
    value: "1"
actions:
  - action: add_label
    value: "auto-responded"
  - action: send_email_transcript
```

### Available Conditions

- Conversation attributes (status, priority, inbox)
- Message content, contact attributes
- Business hours timing

### Available Actions

- Change status, priority, assignee
- Add/remove labels, send message, email transcript
- Mute conversation

See `articles/advanced-features/how-to-use-automation.md`.

## Assignment Rules (V2)

Automatic conversation routing:
- **Round-robin**: Even distribution
- **Capacity-based**: By agent workload
- **Team-based**: Route to specific teams
- **Custom rules**: Match conditions to assignee

See `articles/advanced-features/chatwoot-assignment-v2.md`.
Round-robin: `articles/best-practices/assigning-conversations-in-a-round_robin-fashion.md`

## SLA Policies

Define and enforce response/resolution times:
1. **Settings → SLA → Add policy**
2. Set FRIT (First Response In Time) and NRT (Next Response Time)
3. Configure breach actions (escalate, notify, mark priority)

Setup: `articles/advanced-features/service-level-agreemtns.md`
Reports: `articles/reports/how-to-read-the-sla-reports.md`

## Webhooks

Receive real-time events from Chatwoot:

```bash
# Configure in Settings → Integrations → Webhook
# Events: conversation_created, message_created, contact_created
# POST to your URL with full JSON payload
```

See `articles/apps-integrations/how-to-use-webhooks.md`.

### Webhook Events

- `conversation_created`, `conversation_updated`
- `message_created`, `message_updated`
- `contact_created`, `contact_updated`

## Agent Bots

Automate responses with bots:
- Built-in or custom webhook bots
- Handle common queries before human escalation
- See `articles/features-explained/how-to-use-agent-bots.md`

## Audit Logs

Track all account changes:
- Who did what and when
- Settings changes, agent actions, system events
- See `articles/advanced-features/how-to-use-audit-logs.md`

## Dashboard Apps

Embed third-party tools in the Chatwoot sidebar:
- Custom React/Vue components
- Receive conversation context via postMessage
- Execute Chatwoot API calls
- See `articles/apps-integrations/how-to-use-dashboard-apps.md`

## Custom Attributes

Define custom fields for contacts and conversations:
- Types: text, number, date, dropdown, checkbox
- Use in automations, campaigns, and API
- See `articles/features-explained/how-to-create-and-use-custom-attributes.md`
