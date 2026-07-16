---
name: chatwoot-self-hosted
description: Deploy and maintain a self-hosted Chatwoot instance on Linux VM, Docker, Kubernetes, or cloud providers. Use when installing, configuring, or maintaining a self-hosted Chatwoot server.
---

# Chatwoot Self-Hosted

Deploy and maintain Chatwoot on your own infrastructure.

## Prerequisites

- Docker & Docker Compose (recommended)
- Minimum: 2 CPU, 4GB RAM
- Domain with SSL (Caddy/Let's Encrypt)
- PostgreSQL + Redis (bundled or external)

## Quick Deploy (Docker)

```bash
git clone https://github.com/chatwoot/chatwoot.git
cd chatwoot
cp .env.example .env
# Edit .env with your domain and secrets
docker compose up -d
```

See `references/self-hosted/self-hosted-deployment-docker.md`.

## Deployment Options

| Method | Guide |
|--------|-------|
| Linux VM | `references/self-hosted/self-hosted-deployment-linux-vm.md` |
| Docker | `references/self-hosted/self-hosted-deployment-docker.md` |
| Kubernetes (Helm) | `references/self-hosted/self-hosted-deployment-helm-chart.md` |
| Chatwoot CTL | `references/self-hosted/self-hosted-deployment-chatwoot-ctl.md` |

### Cloud Providers

| Provider | Guide |
|----------|-------|
| AWS | `references/self-hosted/self-hosted-deployment-architecture.md` |
| Azure | `references/self-hosted/self-hosted-deployment-azure.md` |
| DigitalOcean | `references/self-hosted/self-hosted-deployment-digitalocean.md` |
| GCP | `references/self-hosted/self-hosted-deployment-gcp.md` |
| Heroku | `references/self-hosted/self-hosted-deployment-heroku.md` |

## Configuration

| Topic | Guide |
|-------|-------|
| Environment variables | `references/self-hosted/self-hosted-configuration-environment-variables.md` |
| MFA Setup | `references/self-hosted/self-hosted-configuration-multi-factor-authentication.md` |
| SSL Certificate | `articles/help-center/generate-ssl-certificate.md` |

## Integrations Setup

| Integration | Guide |
|-------------|-------|
| Facebook | `references/self-hosted/self-hosted-configuration-features-integrations-facebook-channel-setup.md` |
| Instagram (Facebook login) | `references/self-hosted/self-hosted-configuration-features-integrations-instagram-channel-setup.md` |
| Instagram (Business login) | `references/self-hosted/self-hosted-configuration-features-integrations-instagram-via-instagram-business-login.md` |
| WhatsApp Embedded | `references/self-hosted/self-hosted-configuration-features-integrations-whatsapp-embedded-signup.md` |
| Slack | `references/self-hosted/self-hosted-configuration-features-integrations-slack-integration-setup.md` |
| Linear | `references/self-hosted/self-hosted-configuration-features-integrations-linear-integration-setup.md` |
| Shopify | `references/self-hosted/self-hosted-configuration-features-integrations-shopify-integration-setup.md` |
| TikTok | `references/self-hosted/self-hosted-configuration-features-integrations-tiktok.md` |

## Maintenance

| Task | Guide |
|------|-------|
| Upgrade | `references/self-hosted/self-hosted-deployment-upgrade.md` |
| Backup | `references/self-hosted/self-hosted-deployment-backup.md` |
| Database migration | `references/self-hosted/self-hosted-runbooks-migrate-chatwoot-database.md` |
| v4 Upgrade | `references/self-hosted/self-hosted-runbooks-upgrade-to-chatwoot-v4.md` |
| Email notifications | `references/self-hosted/self-hosted-runbooks-email-notifications.md` |

## Enterprise Edition

Purchase license at chatwoot.com/pricing:
`articles/how-to/purchasing-a-paid-self_hosted-chatwoot-license-a-step_by_step-guide.md`
`articles/other-topics/enterprise-edition.md`
`references/self-hosted/self-hosted-enterprise-edition.md`
