# Chatwoot Skills 🚀

[![CI](https://github.com/fxckcode/chatwoot-skills/actions/workflows/ci.yml/badge.svg)](https://github.com/fxckcode/chatwoot-skills/actions/workflows/ci.yml)
[![License](https://img.shields.io/github/license/fxckcode/chatwoot-skills)](LICENSE)
[![Chatwoot](https://img.shields.io/badge/Chatwoot-7B2FBE?logo=chatwoot)](https://www.chatwoot.com)
[![Agent Skills](https://img.shields.io/badge/Agent%20Skills-Spec-7B2FBE)](https://agentskills.io/specification)

Agent skills for [Chatwoot](https://www.chatwoot.com) — the open-source customer support platform. Use them to integrate Chatwoot into any system: set up channels, configure the live chat widget, automate with Captain AI, use the API, migrate from other platforms, and deploy self-hosted instances.

These skills follow the [Agent Skills specification](https://agentskills.io/specification) so they can be used by any skills-compatible agent, including Claude Code, Codex, Cursor, OpenCode, and Hermes Agent.

## Installation

### via npx skills

```bash
npx skills add fxckcode/chatwoot-skills
```

Or using the full URL:

```bash
npx skills add https://github.com/fxckcode/chatwoot-skills
npx skills add git@github.com:fxckcode/chatwoot-skills.git
```

### via Claude Code

Add the contents of this repo to a `.claude/skills/` directory in your project root:

```bash
git clone https://github.com/fxckcode/chatwoot-skills.git /tmp/chatwoot-skills
cp -r /tmp/chatwoot-skills/skills/* .claude/skills/
```

See the [official Claude Skills documentation](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview#skills) for more details.

### via Cursor

Clone the repo into Cursor's skills directory:

```bash
git clone https://github.com/fxckcode/chatwoot-skills.git ~/.cursor/skills/chatwoot-skills
```

Cursor auto-discovers skills under `~/.cursor/skills/`. Restart Cursor to pick it up.

### via Codex

Copy the `skills/` directory into your Codex skills path:

```bash
git clone https://github.com/fxckcode/chatwoot-skills.git /tmp/chatwoot-skills
cp -r /tmp/chatwoot-skills/skills/* ~/.codex/skills/
```

See the [Agent Skills specification](https://agentskills.io/specification) for the standard skill format.

### via OpenCode

Clone the entire repo into the OpenCode skills directory:

```bash
git clone https://github.com/fxckcode/chatwoot-skills.git ~/.opencode/skills/chatwoot-skills
```

Do not copy only the inner `skills/` folder — clone the full repo so the directory structure is `~/.opencode/skills/chatwoot-skills/skills/<skill-name>/SKILL.md`.

OpenCode auto-discovers all `SKILL.md` files under `~/.opencode/skills/`. No config file changes needed. Skills become available after restarting OpenCode.

### via Hermes Agent

Clone into the Hermes skills directory:

```bash
git clone https://github.com/fxckcode/chatwoot-skills.git ~/.hermes/skills/chatwoot-skills
```

## Skills

| Skill | Description |
|-------|-------------|
| **chatwoot-setup** | Set up a Chatwoot account, configure agents, teams, inboxes, labels, roles, and SAML SSO |
| **chatwoot-channels** | Connect channels — WhatsApp, Facebook, Instagram, Telegram, Email, SMS, Line, TikTok, API inbox, voice |
| **chatwoot-live-chat** | Install and customize the live chat widget on Next.js, Vue, React Native, WordPress, and more |
| **chatwoot-features** | Conversations, CSAT, canned responses, macros, campaigns, labels, priorities, business hours |
| **chatwoot-advanced** | Automation rules, webhooks, SLA policies, assignment rules, agent bots, audit logs |
| **chatwoot-captain** | Set up Captain AI — assistants, FAQ, memories, copilot, custom tools, AI credits |
| **chatwoot-api** | REST API, webhooks, WebSocket, and third-party integrations (Slack, Dialogflow, OpenAI) |
| **chatwoot-reports** | Overview, CSAT, SLA, conversations, agents, and bot reports |
| **chatwoot-migrations** | Migrate from Zendesk, Freshdesk, Intercom, or Front |
| **chatwoot-self-hosted** | Deploy and maintain Chatwoot on Linux VM, Docker, Kubernetes, cloud providers |

## Documentation

The repo also includes the complete Chatwoot User Guide as reference material:

```
articles/             # 136 articles across 15 categories
references/           # 39 self-hosted deployment and developer docs
```

## Repository structure

```
chatwoot-skills/
├── .claude-plugin/
│   ├── plugin.json           # Agent Skills plugin metadata
│   └── marketplace.json      # Marketplace registry
├── skills/
│   ├── chatwoot-setup/       # Account setup, agents, teams
│   ├── chatwoot-channels/    # WhatsApp, Facebook, Instagram, etc.
│   ├── chatwoot-live-chat/   # Widget installation and SDK
│   ├── chatwoot-features/    # Core features
│   ├── chatwoot-advanced/    # Automation, webhooks, SLA
│   ├── chatwoot-captain/     # Captain AI
│   ├── chatwoot-api/         # REST API and integrations
│   ├── chatwoot-reports/     # Reports and analytics
│   ├── chatwoot-migrations/  # Migrate from other platforms
│   └── chatwoot-self-hosted/ # Self-hosted deployment
├── articles/                 # 136 User Guide articles (15 categories)
├── references/               # Deployment and developer docs
├── AGENTS.md                 # AI agent context
├── RULES.md                  # Project conventions
├── .github/                  # CI, release, issue/PR templates
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
