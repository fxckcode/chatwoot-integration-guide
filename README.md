# Chatwoot Integration Guide 🚀

[![CI](https://github.com/fxckcode/chatwoot-integration-guide/actions/workflows/ci.yml/badge.svg)](https://github.com/fxckcode/chatwoot-integration-guide/actions/workflows/ci.yml)
[![License](https://img.shields.io/github/license/fxckcode/chatwoot-integration-guide)](LICENSE)
[![Chatwoot](https://img.shields.io/badge/Chatwoot-7B2FBE?logo=chatwoot)](https://www.chatwoot.com)
[![Markdown](https://img.shields.io/badge/Markdown-000?logo=markdown)](https://daringfireball.net/projects/markdown/)

A comprehensive guide for integrating **Chatwoot** — the open-source customer support platform — into your systems. This repository contains structured documentation, practical examples, and an AI assistant skill that accelerates any Chatwoot integration.

## What's inside

- **SKILL.md** — AI assistant skill for Cursor, Claude Code, Codex, etc. to automatically integrate Chatwoot into projects
- **136+ articles** — Full Chatwoot User Guide documentation categorized in markdown
- **Category-based guides** — Chatwoot 101, setup, channels, features, automation, Captain AI, migrations, and more
- **Practical examples** — Code snippets, configurations, and real-world workflows

## Categories

| Category | Articles | Description |
|----------|----------|-------------|
| 🚀 Chatwoot 101 | Fundamentals | Key concepts, glossary, getting started |
| 🪵 Channels | 10+ | WhatsApp, Facebook, Instagram, Telegram, Email, SMS, Line, TikTok, API |
| 👝 Setup | 8+ | Account, profile, settings, agents, teams, inboxes |
| 📞 Voice | 3+ | Twilio Voice, WhatsApp Voice, configuration |
| 💬 Live Chat | 12+ | Web widget, SDK, React Native, Next.js, Vue, WordPress, GT Mgr |
| 📚 Features | 12+ | CSAT, priorities, signatures, roles, business hours |
| 🔎 Advanced Features | 15+ | Automation, macros, SLA, webhooks, campaigns, assignment rules |
| ⚡ Apps & Integrations | 8+ | Slack, Dialogflow, OpenAI, Google Translate, Linear, Dyte |
| 📊 Reports | 6+ | Overview, CSAT, SLA, conversations, agents, bots |
| ❓ Help Center | 3+ | Setup, SSL, embedding videos |
| 💫 Best Practices | 8+ | Round robin, command bar, shortcuts, folders, segments |
| 🔥 Captain AI | 7+ | AI assistant, FAQ, memories, copilot, custom tools |
| 🛳️ Migrations | 4+ | From Zendesk, Freshdesk, Intercom, Front |
| ⚙️ How To | 12+ | Troubleshooting, push notifications, access tokens, SAML |

## Quick start

### As an AI skill (recommended)

AI assistants that support skills can load `SKILL.md` directly:

```bash
# In Cursor, Claude Code, Codex, OpenCode, etc.
# Point to the skill in this repo
```

### Direct reading

```bash
# Navigate articles by category
ls articles/

# Read a specific article
cat articles/getting-started-chatwoot-101.md

# Search content
grep -ri "webhook" articles/
```

## Repository structure

```
chatwoot-integration-guide/
├── SKILL.md              # Main skill for AI assistants
├── AGENTS.md             # AI agent context
├── RULES.md              # Project conventions
├── articles/             # Categorized documentation
│   ├── chatwoot-101/
│   ├── setup-account/
│   ├── other-channels/
│   ├── voice-channels/
│   ├── website-live-chat/
│   ├── features-explained/
│   ├── advanced-features/
│   ├── apps-integrations/
│   ├── reports/
│   ├── help-center/
│   ├── best-practices/
│   ├── captain/
│   ├── migrations/
│   ├── how-to/
│   └── other-topics/
├── references/           # Technical references
├── .github/              # Templates and workflows
└── README.md
```

## Contributing

1. Fork the repository
2. Create a branch: `git checkout -b feat/my-contribution`
3. Make changes and commit with [Conventional Commits](https://www.conventionalcommits.org/)
4. Push: `git push origin feat/my-contribution`
5. Open a Pull Request

## License

MIT — see [LICENSE](LICENSE) for details.

---

Built with ❤️ by [fxckcode](https://github.com/fxckcode) for the Chatwoot community.
