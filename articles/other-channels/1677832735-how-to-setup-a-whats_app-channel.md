# How to setup a WhatsApp channel?

You can manage your WhatsApp Business Account conversations directly from Chatwoot. To connect your WhatsApp number, Chatwoot supports two onboarding methods:

* **Embedded Signup (recommended)** – a guided flow powered by Meta that auto-configures your number, webhooks, and tokens.

* **Manual Setup** – an advanced option for tech providers and cases where Embedded Signup cannot be used.

This guide gives you an overview of both methods, their differences, and links to detailed step-by-step instructions.

## Prerequisites

* A **Meta (Facebook) developer or business account**

* A **valid phone number** (not already tied to another WhatsApp Embedded Signup flow, unless migrating)

* A **Chatwoot workspace** with WhatsApp feature enabled

## Step 1: Go to Inboxes

1. Log into your Chatwoot account.

2. Navigate to **Settings › Inboxes › Add Inbox**.

3. Choose **WhatsApp** as the channel.

## Step 2: Choose Your Setup Method

When creating a WhatsApp Inbox, you’ll see two options:

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSXdHUWdJPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--110e3b519bfa6e18081c32a9c1a807f80c95b390/CleanShot-202025-09-02-20at-2013.21.42@2x.png)**Connect with Whatsapp Business (Embedded Signup)**

* Redirects you to Meta’s Embedded Signup flow.

* You log in with your Facebook account, select or create a WhatsApp Business Account (WABA), and add your phone number.

* Chatwoot automatically receives the webhook, tokens, and phone number configuration.

Use this option if you are:

* Adding a **new WhatsApp number**

* Looking for the **fastest, no-configuration setup**

* Not a tech provider onboarding your own number

[Read the full guide on WhatsApp Embedded Signup](https://www.chatwoot.com/hc/user-guide/articles/1752129193-how-to-use-whatsapp-embedded-signup)

### **Manual Setup**

* You configure everything through the Meta Developer Console.

* Requires generating tokens, creating a system user, assigning assets, and setting up webhooks manually.

* You copy/paste the Phone Number ID, Business Account ID, and API key into Chatwoot.

Use this option if you are:

* A **tech provider** onboarding your own number

* Reusing a number that is **already linked to Embedded Signup**

* Comfortable working with the Meta Developer dashboard

[Read the full guide on Manual Setup](https://www.chatwoot.com/hc/user-guide/articles/1756799850-how-to-setup-a-whats_app-channel-manual-flow)

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTXNHUWdJPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--21bc9986897a4a6d67f3b94b798403548edaa37f/CleanShot-202025-09-02-20at-2013.32.54@2x.png)
