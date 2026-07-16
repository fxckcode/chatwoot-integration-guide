# Lesson 1: Your first Chatwoot conversation

Welcome to Chatwoot! This is the first stop in a hands-on series that takes you from a brand-new account to a fully running support desk. By the end of this lesson, you'll have a working website inbox and you'll have replied to your very first customer message.

## What you'll learn

* What Chatwoot is and how it fits into your support stack

* What channels and inboxes are, and how they relate

* How a customer message becomes a conversation on your dashboard

* How to set up a website live chat inbox in under five minutes

* How to send your first reply and resolve the conversation

**You'll need:** A Chatwoot account (free trial works) and any website where you can paste a snippet of code. Don't have a site handy? You can test on a local HTML file.

---

## What is Chatwoot?

Chatwoot is a single dashboard for every customer conversation your business has — email, website live chat, WhatsApp, Instagram, Facebook, SMS, Telegram, and more. Instead of switching between five different apps and losing track of who said what, your team works out of one place, with shared context, history, and tools.

Think of it as your team's **shared inbox for customers** — but with the automation, reporting, and AI helpers a real support team needs.

\
![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRVQrSUFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--5018122350b902c5f14c7f42f26b754751e1a922/conversation.png)

---

## Channels and inboxes (the one concept to understand first)

A **channel** is a *type* of communication — Email, Website, WhatsApp, SMS, etc.

An **inbox** is a *specific instance* of a channel that's connected to your account. For example:

* "support[@]acme.com" is an email inbox

* The chat widget on `acme.com` is a website inbox

* Your `+1-555-…` WhatsApp number is a WhatsApp inbox

You can have as many inboxes as you need, even multiple of the same type (one website inbox for marketing, another for billing).  \
 \
Every message that comes in lives inside an inbox, and every inbox can have its own agents, business hours, greeting, and routing rules.

> **Tip:** Don't overthink your inbox layout on day one. Start with one, get comfortable, then split it up as your team grows.

---

## How a message becomes a conversation

Here's the lifecycle of a single customer message — keep this in mind as you go through the rest of the product:

1. **Customer sends a message** on one of your channels (e.g. types into your website widget).

2. **Chatwoot creates a conversation** in the matching inbox. The conversation starts in the **Open** status or in **Pending** status if Captain is connected.

3. **An agent is assigned** — automatically (via assignment policy) or manually.

4. **Agent replies** from the dashboard. The reply goes back to the customer over the *same* channel they wrote in on.

5. **The conversation is resolved** when the issue is handled. It's not deleted — the full history stays searchable, attached to the contact.

Conversations have four common statuses: **Open**, **Pending**, **Snoozed**, and **Resolved**. You'll meet all of them as you go.

---

## Set up your first inbox: Website live chat

We'll use the website channel because it's the fastest way to see Chatwoot working end-to-end.

### Step 1 — Open the inbox setup

From the dashboard, go to **Settings → Inboxes → Add Inbox**.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCR1grSUFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b494013b98d6e98e90e0fde14f4b88b4bc56d63c/setup-inbox.png)

### Step 2 — Pick "Website"

You'll see a grid of channel types. Click the **Website** icon.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSGIrSUFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--4cb6259af3dd18aeee9a14c11079873683970036/web-channel.png)

### Step 3 — Fill in the basics

* **Website Name** — what your customers will see at the top of the chat widget (e.g. *Acme Support*).

* **Website Domain** — the URL where the widget will live (e.g. `https://acme.com`).

* **Widget Color** — pick something on-brand.

* **Welcome Heading & Tagline** — the first thing visitors read when they open the widget.

### Step 4 — Add agents

Choose which teammates can reply to messages from this inbox. You can add or remove people later.

### Step 5 — Install the snippet

Chatwoot will hand you a small JavaScript snippet. Paste it into your site's `<head>` (or just before `</body>`). Reload your page and you should see the chat bubble in the corner.

***No website yet?** You don't need one to test. Go to **Settings → Inboxes**, click the **gear icon** next to your new inbox to open its settings, then open the **Configuration** tab and click **Open in Codepen** on the script. A live widget will open in your browser where you can send messages straight away.*

### Step 6 — Send a test message

Click the chat bubble on your site, type *"Hello from my first visitor!"* and hit send.

### Step 7 — Reply from the dashboard

Switch back to your Chatwoot dashboard. The new conversation will appear at the top of your conversation list with an unread badge. Click it, type your reply in the chat box at the bottom, and hit send. The customer will see it instantly in the widget.

🎉 You've just handled your first Chatwoot conversation.

---

## A quick tour of the conversation view

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSTcrSUFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--2f9a3ad0eebda3d110419f883daa4e08e5289d2b/responding-msg.png)

Once you're inside a conversation, here's what each part does — at a glance:

| Area                         | What it's for                                                                         |
| ---------------------------- | ------------------------------------------------------------------------------------- |
| **Reply box**                | Send public replies to the customer                                                   |
| **Private Notes**            | Discuss the conversation with teammates — the customer never sees these               |
| **Right sidebar**            | Customer details, conversation actions, custom attributes, and previous conversations |
| **Conversation actions**     | Assign an agent, change status, snooze, add labels                                    |
| **Conversation list (left)** | Filter by status, assignee, inbox, label, or saved folder                             |

You don't need to use any of these on day one. Replying from the chat box is enough to support real customers.

---

## Resolving the conversation

When you're done helping the customer:

1. Click **Resolve** at the top of the conversation.

2. The conversation moves out of your **Open** queue and into **Resolved**.

3. If you've enabled CSAT, the customer is automatically asked to rate the experience.

If the customer replies after resolving, the conversation **automatically reopens** — nothing falls through the cracks.

---

## Try these next (optional, 1 minute each)

While you're here, poke at one or two of these so they're not strangers later:

* **Set your status to Online** — top right avatar → *Online / Busy / Offline*.

* **Send a private note** — type `@teammate looks like a billing issue` in the Private Notes tab.

* **Add a label** — try `bug-report` or `feature-request` from the top bar.

* **Snooze the conversation** — useful for "waiting on customer" cases.

---

## Common first-day questions

**Will the customer see my name?**

Yes — your display name and avatar from Profile Settings appear on outgoing replies. Take a minute to set both before you reply to a real customer.

**What if I reply to the wrong person?**

You can delete a message you sent (on live chat widget, it is not supported in other channels). After that, send a follow-up correction — the original stays in dashboard with a deleted message for accuracy, the customer doesn't see it again.

**Can two agents work on the same conversation?**

Yes. One agent is the **Assignee** (owns the reply); others can be added as **Conversation Participants** to follow along and chime in.

**Is anything I type in the chat box sent immediately?**

No. Replies only send when you click **Send** (or hit ⌘/Ctrl+Enter). And if you navigate away mid-message, Chatwoot keeps a **Draft Reply** so you don't lose your work.

---

## What's next

In [**Lesson 2**](https://www.chatwoot.com/hc/chatwoot-user-guide-cloud-version/articles/1677231493-lesson-2-dashboard-basics), we'll go beyond the reply box: private notes, canned responses, labels, and how to keep your queue tidy as conversations pile up.

Until then, your homework is simple: **send yourself three test messages from the widget and reply to each one.** Muscle memory beats theory.

Welcome aboard. 👋
