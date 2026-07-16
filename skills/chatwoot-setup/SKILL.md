---
name: chatwoot-setup
description: Set up a Chatwoot account, configure agents, teams, inboxes, labels, roles, SAML SSO, and notification preferences. Use when the user needs to create or configure a Chatwoot workspace.
---

# Chatwoot Setup

Set up and configure a Chatwoot workspace for production use.

## Account & Workspace

1. Go to https://app.chatwoot.com and sign up
2. Confirm email and set workspace name
3. Complete or skip onboarding wizard

See `articles/setup-account/create-your-chatwoot-account.md`.

## Profile & General Settings

| Setting | Article |
|---------|---------|
| Personal profile | `articles/setup-account/customizing-your-personal-profile.md` |
| General settings | `articles/setup-account/customizing-your-general-settings.md` |
| Notifications | `articles/setup-account/setting-up-notifications.md` |

## Agents

Add agents via **Settings → Agent Management**:
- Agents receive email invitations
- Roles: **Agent** (default), **Administrator** (full access)
- Granular roles available in v3.18+ (`articles/features-explained/manage-team-access-control-with-flexible-role_based-permissions.md`)

See `articles/setup-account/adding-agents.md`.

## Teams

**Settings → Teams** → Create team, add agents:
- Route conversations to specific teams
- Filter by team in reports

See `articles/setup-account/adding-teams.md`.

## Inboxes

**Settings → Inboxes** → Add inbox:
- Each inbox connects to a channel (WhatsApp, Email, Website, etc.)
- Configure auto-assignment, collaborators, and business hours

See `articles/setup-account/adding-inboxes.md`.

## Labels

**Settings → Labels**:
- Color-coded categories for conversations
- Apply from conversation side panel
- Display on sidebar for filtering

See `articles/features-explained/how-to-add-labels.md`.

## Custom Attributes

Define custom fields for contacts and conversations:
- Types: text, number, date, dropdown, checkbox
- Use in automations, campaigns, and API

See `articles/features-explained/how-to-create-and-use-custom-attributes.md`.

## SAML SSO

Enterprise feature:
- **Settings → Login & Authentication**
- Supports Okta, Azure AD, Google Workspace

See `articles/advanced-features/setting-up-saml.md`.

## Agent Capacity

Limit concurrent conversations per agent:
- **Settings → Agent Capacity**
- Prevents overload

See `articles/advanced-features/agent-capacity.md`.
