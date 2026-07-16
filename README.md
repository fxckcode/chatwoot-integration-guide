# Chatwoot Integration Guide 🚀

[![CI](https://github.com/fxckcode/chatwoot-integration-guide/actions/workflows/ci.yml/badge.svg)](https://github.com/fxckcode/chatwoot-integration-guide/actions/workflows/ci.yml)
[![License](https://img.shields.io/github/license/fxckcode/chatwoot-integration-guide)](LICENSE)
[![Chatwoot](https://img.shields.io/badge/Chatwoot-7B2FBE?logo=chatwoot)](https://www.chatwoot.com)
[![Agent Skills](https://img.shields.io/badge/Agent%20Skills-Spec-7B2FBE)](https://agentskills.io/specification)

A comprehensive guide for integrating **Chatwoot** — the open-source customer support platform — into your systems. This repository contains structured documentation, practical examples, and an AI agent skill that accelerates any Chatwoot integration.

These skills follow the [Agent Skills specification](https://agentskills.io/specification) so they can be used by any skills-compatible agent, including Claude Code, Codex, Cursor, OpenCode, and Hermes Agent.

## Installation

### via npx skills

```bash
npx skills add fxckcode/chatwoot-integration-guide
```

Or using the full URL:

```bash
npx skills add https://github.com/fxckcode/chatwoot-integration-guide
npx skills add git@github.com:fxckcode/chatwoot-integration-guide.git
```

### via Claude Code

Add the contents of this repo to a `.claude/skills/` directory in your project root:

```bash
git clone https://github.com/fxckcode/chatwoot-integration-guide.git /tmp/chatwoot-skills
cp -r /tmp/chatwoot-skills/skills/chatwoot .claude/skills/chatwoot
```

See the [official Claude Skills documentation](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview#skills) for more details.

### via Cursor

Clone the repo and symlink the skill into Cursor's skills directory:

```bash
git clone https://github.com/fxckcode/chatwoot-integration-guide.git ~/.cursor/skills/chatwoot-integration-guide
```

Cursor auto-discovers skills under `~/.cursor/skills/`. Restart Cursor to pick it up.

### via Codex

Copy the `skills/` directory into your Codex skills path:

```bash
git clone https://github.com/fxckcode/chatwoot-integration-guide.git /tmp/chatwoot-skills
cp -r /tmp/chatwoot-skills/skills/chatwoot ~/.codex/skills/chatwoot
```

See the [Agent Skills specification](https://agentskills.io/specification) for the standard skill format.

### via OpenCode

Clone the entire repo into the OpenCode skills directory:

```bash
git clone https://github.com/fxckcode/chatwoot-integration-guide.git ~/.opencode/skills/chatwoot-integration-guide
```

Do not copy only the inner `skills/` folder — clone the full repo so the directory structure is `~/.opencode/skills/chatwoot-integration-guide/skills/chatwoot/SKILL.md`.

OpenCode auto-discovers all `SKILL.md` files under `~/.opencode/skills/`. No config file changes needed. Skills become available after restarting OpenCode.

### via Hermes Agent

```bash
hermes skill install chatwoot
```

Or clone and symlink from the Hermes skills directory:

```bash
git clone https://github.com/fxckcode/chatwoot-integration-guide.git ~/.hermes/skills/chatwoot-integration-guide
```

## What's inside

- **AI skill** (`skills/chatwoot/SKILL.md`) — For Claude Code, Codex, Cursor, OpenCode, Hermes, and any Agent Skills-compatible agent
- **136+ articles** — Full Chatwoot User Guide documentation categorized in markdown
- **Category-based guides** — Chatwoot 101, setup, channels, features, automation, Captain AI, migrations, and more
- **Practical examples** — Code snippets, configurations, and real-world workflows
- **Self-hosted docs** — 39 pages covering deployment on Linux VM, Docker, Kubernetes, cloud providers

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

## Repository structure

```
chatwoot-integration-guide/
├── .claude-plugin/
│   ├── plugin.json           # Agent Skills plugin metadata
│   └── marketplace.json      # Marketplace registry
├── skills/
│   └── chatwoot/
│       └── SKILL.md          # Main AI agent skill
├── articles/                 # Categorized documentation
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
├── references/
│   └── self-hosted/          # Deployment and developer docs
├── AGENTS.md                 # AI agent context
├── RULES.md                  # Project conventions
├── .github/                  # CI, release, issue/PR templates
└── README.md
```

## Skills

| Skill | Description |
|-------|-------------|
| **chatwoot** | Integrate Chatwoot into any system — setup channels, live chat widget, Captain AI, webhooks, API, and migrations |

## Direct reading

```bash
# Navigate articles by category
ls articles/

# Read a specific article
cat articles/chatwoot-101/getting-started-chatwoot-101.md

# Search content
grep -ri "webhook" articles/
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
