---
name: chatwoot-captain
description: Set up and use Captain AI — Chatwoot's built-in AI agent for automated customer support. Use when configuring AI assistants, FAQ bots, copilot features, or custom tools for Captain.
---

# Chatwoot Captain AI

Captain is Chatwoot's built-in AI assistant for automated customer support.

## Setup

1. **Settings → Captain** → Enable
2. Create an assistant with personality/prompt
3. Connect to an inbox
4. Configure auto-resolution

See `articles/captain/captain-_-introduction.md`.
See `articles/captain/creating-an-assistant-with-captain.md`.

## Knowledge Base (FAQ)

Upload documents for Captain to reference:
- Supported: PDF, DOCX, TXT, MD
- Create Q&A pairs manually

See `articles/captain/creating-an-faq-with-captain.md`.
See `articles/captain/creating-a-document-in-captain.md`.

## Memories

Captain remembers facts about contacts across conversations:
- Automatically extracted from chat history
- Manually addable via Memories panel

See `articles/captain/how-to-use-captain-memories.md`.

## Copilot

Agents use Captain as a copilot:
- Suggest replies
- Summarize conversations
- Research from connected sources

See `articles/captain/how-to-use-captain-copilot.md`.

## Custom Tools

Extend Captain with API-connected tools:

1. Navigate to **Captain → Tools → Create**
2. Define: name, description (most important!), method, endpoint URL
3. Add parameters for data extraction
4. Configure auth (Bearer, Basic, API Key, or None)

### Context Sent to Your API

Captain includes metadata headers with every tool call:
- `X-Chatwoot-Account-Id`, `X-Chatwoot-Conversation-Id`
- `X-Chatwoot-Contact-Email`, `X-Chatwoot-Contact-Id`
- `X-Chatwoot-Contact-Inbox-Verified` (HMAC check)

### Limits

- Max 15 tools per account (recommended ≤ 10)
- 30-second timeout, 1 MB response cap
- HTTPS only, no localhost/private IPs

See `articles/captain/v2-_-how-to-set-up-custom-tools-for-captain.md`.

## Self-Hosted Captain

Requires OpenAI API key or Ollama endpoint:
See `articles/captain/how-to-enable-captain-on-self_hosted-installations.md`.

## AI Credits

AI operations consume credits. Purchase credits or subscribe.
See `articles/captain/how-ai-credits-work-in-captain.md`.

## Website Crawling

Allow Captain to crawl your site:
Update `robots.txt` to allow `FirecrawlAgent`.
See `articles/captain/updating-robots-txt-to-allow-chatwoot-assistant-to-crawl-your-website.md`.
