---
name: chatwoot-channels
description: Connect and configure Chatwoot channels — WhatsApp, Facebook, Instagram, Telegram, Email, SMS, Line, TikTok, API inbox, and voice (Twilio). Use when setting up a messaging channel or inbox.
---

# Chatwoot Channels

Connect messaging channels to Chatwoot inboxes. Each channel type has specific setup steps and requirements.

## WhatsApp

| Method | Best for | Article |
|--------|----------|---------|
| **Meta Embedded Signup** | Easy, official | `articles/other-channels/how-to-use-whatsapp-embedded-signup.md` |
| **Manual (Meta)** | Existing Meta setup | `articles/other-channels/how-to-setup-a-whats_app-channel-manual-flow.md` |
| **Twilio** | Twilio customers | `articles/other-channels/how-to-set-up-a-whats_app-channel-with-twilio.md` |

### WhatsApp Templates

- Templates need Meta approval for proactive messaging
- See `articles/advanced-features/whatsapp-templates.md`
- Twilio content templates: `articles/advanced-features/twilio-content-templates.md`

### WhatsApp CSAT

CSAT surveys work on WhatsApp:
`articles/features-explained/whats_app-csat-surveys-in-chatwoot.md`

### Common Issues

- Brazil/Argentina number quirks: `articles/other-topics/inconsistencies-for-whats_app-numbers-in-brazil-mexico-and-argentina.md`
- General issues: `articles/advanced-features/common-whats_app-issues-and-how-to-fix-them.md`
- Migrate embedded to manual: `articles/other-topics/migrate-a-whats_app-embedded-signup-inbox-to-manual-setup.md`

## Facebook & Instagram

| Channel | Article |
|---------|---------|
| Facebook Page | `articles/other-channels/how-to-setup-a-facebook-channel.md` |
| Instagram (via Facebook) | `articles/other-channels/how-to-setup-an-instagram-channel.md` |
| Instagram (direct login) | `articles/other-channels/how-to-setup-an-instagram-channel-via-instagram-login.md` |
| Human Agent Tag | `articles/advanced-features/what-is-human-agent-tag-in-instagram-messenger-channel.md` |

## Email

Connect any IMAP/SMTP email:
```yaml
IMAP: imap.example.com:993 (SSL)
SMTP: smtp.example.com:587 (TLS)
```
See `articles/other-channels/how-to-setup-an-email-channel.md`.

## SMS (Twilio)

Uses Twilio messaging service, supports short and long codes.
See `articles/other-channels/how-to-setup-an-sms-channel.md`.

## Other Channels

| Channel | Article |
|---------|---------|
| Twitter | `articles/other-channels/how-to-setup-a-twitter-channel.md` |
| Telegram | `articles/other-channels/how-to-setup-a-telegram-channel.md` |
| Line | `articles/other-channels/how-to-setup-a-line-channel.md` |
| TikTok | `articles/other-channels/how-to-setup-a-tik_tok-channel.md` |
| API Inbox | `articles/other-channels/how-to-create-an-api-channel-inbox.md` |

## Voice Channels

| Provider | Article |
|----------|---------|
| Twilio Voice | `articles/voice-channels/connecting-twilio-voice-channel.md` |
| WhatsApp Voice | `articles/voice-channels/connecting-whats_app-voice-channel.md` |
| Voice Overview | `articles/voice-channels/voice-calling-in-chatwoot.md` |
