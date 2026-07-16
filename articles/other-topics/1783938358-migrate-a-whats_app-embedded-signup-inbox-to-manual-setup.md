# Migrate a WhatsApp Embedded Signup inbox to manual setup

This guide helps you move an existing WhatsApp Cloud inbox to manual setup in Chatwoot. The migration keeps your existing inbox intact. Conversations, contacts, collaborators, routing rules, business hours, CSAT settings, bot settings, and other inbox settings are preserved.

> **Whatsapp number with coexistence support is currently under review. If your WhatsApp number is also used in the WhatsApp Business App, contact Chatwoot Support before starting this migration.**

Before starting the migration, make sure you have the required WhatsApp Cloud API details from Meta.

If you need help creating a Meta app, finding your WABA ID and Phone Number ID, generating an access token, or configuring the required permissions, follow this [guide](https://www.chatwoot.com/hc/user-guide/articles/1756799850-how-to-setup-a-whats_app-channel-manual-flow) first.

## Start the migration

1. Go to **Settings → Inboxes**.

2. Open the affected WhatsApp inbox.

3. Click **Start manual migration**.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRllnMndVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--0fed8e7f92b6a0dacb1a1ca68422eeec6a431a47/CleanShot%202026-07-13%20at%2014.28.42@2x.png)

Chatwoot will open a guided migration flow.

## Step 1: Review what will change

The first step explains what will be preserved and what will be updated.

Preserved:

* Conversations

* Contacts

* Collaborators

* Routing

* Business hours

* Inbox settings

Updated:

* WABA ID

* Phone Number ID

* Access token

* Webhook configuration

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCT01nMndVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--9e1d089787f62140ca6ee62fb27f44417f083d5c/CleanShot%202026-07-13%20at%2014.30.08@2x.png)

Click **Continue**.

## Step 2: Enter business details

Enter the WhatsApp asset details from Meta.

Fields:

* **WABA ID**: The WhatsApp Business Account that owns this phone number.

* **Phone Number ID**: Meta’s unique ID for the WhatsApp number connected to this inbox.

* **Display phone number**: The customer-facing WhatsApp number. This cannot be changed during migration.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRkFrMndVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--3554a80c878cdecba4de08b8c42ed6cb1a5a98fd/CleanShot%202026-07-13%20at%2014.35.38@2x.png)

Click **Continue**.

## Step 3: Add the access token

Paste a permanent access token or system user token with WhatsApp permissions.

The token must include:

* `whatsapp_business_messaging`

* `whatsapp_business_management`

`whatsapp_business_messaging` is required for messaging. `whatsapp_business_management` is required for template sync and template management.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSTBrMndVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--365e188d56d91c2b5adf3f3030e484f0e71d9614/CleanShot%202026-07-13%20at%2014.36.18@2x.png)

## Step 4: Review and reconnect

Review the inbox, phone number, WABA ID, and Phone Number ID before applying changes.

Chatwoot will verify the credentials with Meta before applying changes. If verification fails, the current configuration is left untouched.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRThsMndVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--57a16743b6aad7c8870c8e50e96c37ef93e271a7/CleanShot%202026-07-13%20at%2014.37.18@2x.png)

Click **Reconnect WhatsApp inbox** to complete the migration.

## After migration

After the migration succeeds, the inbox remains the same in Chatwoot, but the WhatsApp connection uses the manual WhatsApp Cloud API setup.

You should verify:

* Incoming messages

* Outgoing replies

* Template message sending

* Template sync

* Webhook delivery

## Need help?

If you are unsure about any step, contact Chatwoot Support. We can help you verify the required Meta details and assist with the migration.
