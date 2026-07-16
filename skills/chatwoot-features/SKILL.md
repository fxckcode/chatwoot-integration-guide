---
name: chatwoot-features
description: Use Chatwoot core features — conversations, CSAT surveys, canned responses, macros, campaigns, labels, priorities, business hours, omnichannel signatures, and interactive messages. Use when managing conversations or configuring workspace features.
---

# Chatwoot Features

Core features for managing conversations and customer interactions.

## Conversations

| Feature | Article |
|---------|---------|
| Conversation filters | `articles/advanced-features/how-to-use-conversation-filters.md` |
| Priority assignment | `articles/features-explained/how-to-assign-a-priority.md` |
| Sorting | `articles/advanced-features/how-does-sorting-work.md` |
| CSAT surveys | `articles/features-explained/how-to-enable-csat-surveys.md` |
| WhatsApp CSAT | `articles/features-explained/whats_app-csat-surveys-in-chatwoot.md` |
| CSAT review notes | `articles/features-explained/review-notes-for-csat.md` |
| Agent collision prevention | `articles/features-explained/preventing-agent-collision.md` |
| Business hours & auto-responder | `articles/features-explained/business-hours-and-auto_responder.md` |
| Required attributes | `articles/advanced-features/required-conversation-attributes.md` |

## Canned Responses (Saved Replies)

1. **Settings → Canned Responses → Add**
2. Set a shortcut (`!greeting`)
3. Type `!greeting` in conversation to expand

See `articles/features-explained/how-to-create-saved-reply-templates-with-canned-responses.md`.

## Macros

Pre-defined actions applied to conversations:
- Assign, add label, send message, change status
- Apply manually or via automation
- See `articles/advanced-features/how-to-use-macros.md`

## Campaigns

| Type | Use Case |
|------|----------|
| **One-off** | Broadcast to segment |
| **Ongoing** | Automated drip campaigns |
| **Widget campaigns** | In-app messages on websites |

See `articles/advanced-features/how-to-use-campaigns.md`.
Wildcard URLs: `articles/advanced-features/wildcard-url-support-in-website-live_chat-campaigns.md`

## Labels

Color-coded categories for organizing conversations:
- Create in **Settings → Labels**
- Apply from conversation side panel
- See `articles/features-explained/how-to-add-labels.md`

## Interactive Messages

Send structured messages with buttons:
- Cards with images, titles, descriptions
- Action buttons (link, postback)
- See `articles/advanced-features/how-to-use-interactive-messages.md`

## Omnichannel Message Signature

Set different signatures per channel:
- HTML-supported, channel-specific (email vs WhatsApp)
- See `articles/features-explained/how-to-use-the-omnichannel-message-signature.md`

## Template Variables

Dynamic variables in messages:
```
Hello {{contact.name}},
Ticket {{conversation.display_id}} updated.
Status: {{conversation.status}}
```
See `articles/advanced-features/template-variables.md`.
