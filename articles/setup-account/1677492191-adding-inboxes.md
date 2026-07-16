# What is a channel? What is an inbox?

A **channel** is a *type* of communication — Website, Email, WhatsApp, SMS, etc. An **inbox** is a *specific instance* of a channel connected to your account. You can have multiple inboxes of the same channel type — e.g. one Website inbox for your marketing site and another for your help center, or two WhatsApp numbers for different regions.

Every conversation in Chatwoot lives inside an inbox. Inboxes carry their own agents, business hours, greetings, pre-chat form, and routing rules.

**Where to set up:** **Settings → Inboxes → Add Inbox** opens the channel picker. Pick the channel type, fill in the credentials/settings, add agents, and finish.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTUhsSXdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--6e29ae8931840443f9597c9ec3ca296aacd7d396/create-inbox.jpg)

\
This doc lists every channel type Chatwoot supports, what you need to configure for each, and the settings tabs that appear on every inbox once it exists.

---

## The channel types

### Website (live chat widget)

The classic chat bubble on your website — the most popular starting channel and the fastest to set up. You give the inbox a name, point it at the website it'll live on, pick a brand color, and write the welcome heading and tagline that visitors see when they open the widget. After saving, Chatwoot hands you a small snippet of code to paste into your site, and the widget is live.

### Email

For handling support email inside Chatwoot. You can connect a Gmail or Google Workspace mailbox by signing in with Google, a Microsoft 365 mailbox by signing in with Microsoft, or any other email provider by entering your incoming and outgoing email server details manually.

### Facebook Messenger

For receiving and replying to direct messages sent to your Facebook Page. Sign in to Facebook through Chatwoot, pick the Page you want messages from, and you're done. From then on, every Page DM lands in your dashboard as a conversation, ready for your team to reply alongside their other channels.

### Instagram (DM)

For Instagram Direct Messages. Connect your Instagram Business account through the Meta sign-in flow — typically through the Facebook Page that's linked to your Instagram account. Once connected, your IG DMs flow into Chatwoot with the same reply, label, and assignment workflow as any other channel.

### TikTok

For TikTok Business messages. Sign in to your TikTok Business account through Chatwoot's connection flow, and customer messages on TikTok land in your Chatwoot inbox.

### WhatsApp

For two-way conversations on WhatsApp, WhatsApp Cloud API is the recommended choice for new accounts. Connect your phone number and Business Account using Meta's embedded sign-up flow inside Chatwoot.

Once connected, the message templates approved on your WhatsApp Business Account sync automatically into Chatwoot. Templates are how you start outbound conversations and re-engage customers outside the 24-hour customer-service window — WhatsApp's policy requires a pre-approved template for those messages, so they need to be created and approved on Meta's side before they're available to send from Chatwoot.

### SMS

For text-message conversations. Chatwoot supports two SMS providers:

* **Twilio** — connect your Twilio phone number and the credentials Twilio gives you for messaging.

* **Bandwidth** — connect your Bandwidth phone number and the credentials Bandwidth gives you.

Once set up, customer texts arrive in your dashboard as conversations and replies your team sends are delivered as SMS to the customer's phone.

### Telegram

For a Telegram bot. Create a bot in Telegram by chatting with [BotFather](https://t.me/botfather) (Telegram's official bot for creating bots), copy the **bot token** it gives you, and paste it into Chatwoot. Your inbox now receives every message a customer sends to your bot.

### LINE

For a LINE Official Account. Get your channel credentials from LINE Developers, paste them into Chatwoot, and customer messages on your LINE account arrive as conversations.

### API Channel

For anything that isn't one of the built-in channel types. The API channel lets you connect a custom application — for example, a niche messaging platform Chatwoot doesn't yet support natively, or an in-product chat experience inside your own software. You provide a destination URL where Chatwoot should send outbound messages, and your application is responsible for relaying them onward.

---

## Common inbox-level options

A few options apply across most channels and live on the **Settings** or **Configuration** tabs:

* **Auto-assignment** — when on, new conversations are distributed to inbox agents. See Auto Assignment.

* **Lock to single conversation** — for channels that don't have native threading (SMS, WhatsApp, Facebook, Instagram, API, LINE, TikTok, Telegram), enabling this means each contact has at most one open conversation at a time. New messages reopen the existing conversation rather than creating a new one.

* **Continuity via email** — for Website inboxes, customers can reply to email transcripts and have replies land back in the same conversation.

* **Sender name** — choose between *Friendly* (just the agent's display name) or *Professional* (display name + business name) on outbound messages.

* **Greeting** — toggle and message; the greeting auto-sends when a new conversation begins on this inbox.

---

## Frequently asked questions

**Can I have more than one inbox of the same type?**

Yes. Multiple Website inboxes, multiple WhatsApp numbers, multiple email addresses — no limit on type.

**An agent doesn't see the inbox in their queue. Why?**

Inbox membership is explicit. Add them under the **Collaborators** tab. Adding an agent to your account doesn't automatically give them access to every inbox.

**What happens if I delete an inbox?**

The inbox and all its conversations are permanently removed. Export anything you need to keep first. Deletion is irreversible.

**Are conversations the same contact across channels?**

A single contact can have conversations on multiple channels — the contact record is account-wide. The conversation lives inside the inbox the message arrived on, but you'll see all the contact's conversations in their profile.

**Which channels support outbound campaigns?**

Live-chat campaigns work on Website inboxes. One-off campaigns can use SMS or WhatsApp Cloud API.

## Next steps[​](https://www.chatwoot.com/docs/user-guide/add-inbox-settings#next-steps "Direct link to heading")

Find the detailed steps to configure each channel below.

* [Website channel](https://www.chatwoot.com/docs/product/channels/live-chat/create-website-channel)

* [Facebook messenger channel](https://www.chatwoot.com/docs/product/channels/facebook)

* [WhatsApp channel](https://www.chatwoot.com/docs/product/channels/whatsapp/whatsapp-cloud)

* [SMS channel](https://www.chatwoot.com/docs/product/channels/sms/twilio)

* [Email channel](https://www.chatwoot.com/docs/product/channels/email/create-channel)

* [Connect a channel using API](https://www.chatwoot.com/docs/product/channels/api/create-channel)

* [Telegram channel](https://www.chatwoot.com/docs/product/channels/telegram)

* [Line channel](https://www.chatwoot.com/docs/product/channels/line)

Next: [Adding teams](https://www.chatwoot.com/hc/user-guide/articles/1677492970-adding-teams)

**Number of inboxes are subject to a fair use policy based on number of agents and subscribed plan.*
