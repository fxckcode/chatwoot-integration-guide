# AGENTS.md — Chatwoot Skills

## Project Overview

Agent skills for Chatwoot — the open-source customer support platform. Contains 10 granular skills plus the full Chatwoot User Guide as reference material.

**Tech Stack**: Markdown, YAML

## Architecture

```
skills/             → 10 granular skills (setup, channels, live-chat, features, advanced, captain, api, reports, migrations, self-hosted)
articles/           → 136 User Guide articles across 15 categories
references/         → 39 self-hosted deployment docs
.github/            → CI and community templates
```

## Key Conventions

| Rule | Standard |
|------|----------|
| **Language** | English |
| **Naming** | kebab-case for files and skills |
| **Formatting** | Prettier for markdown |
| **Commits** | Conventional commits |

## For AI Agents

Before helping with this repo:
1. Each skill in `skills/<name>/SKILL.md` covers a focused area — check descriptions to pick the right one
2. Use `articles/` for deep reference material on specific features
3. Use `references/self-hosted/` for deployment and configuration details
