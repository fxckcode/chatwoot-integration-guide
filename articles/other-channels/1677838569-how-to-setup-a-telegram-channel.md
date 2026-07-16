# How to setup a Telegram channel?

**Step 1**. Go to Settings → Inboxes → “Add Inbox”.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBK2lrVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--c6bd8b490ea436c82352af36043f4be5579c4e00/adding%20an%20inbox%20in%20chatwoot.png)

**Step 2.** Click on the "Telegram" icon.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBd2FsVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--f91ae3d92d61fe207bb02f31516dbc746f8a6b63/telegram%20inbox%20in%20chatwoot.png)

**Step 3.** Create a new telegram bot using Telegram [BotFather](https://telegram.me/BotFather).

**Step 4**. Enter the API token of the Telegram bot and click on "Create Telegram Channel".

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBL3lrVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--c34c4e63ad1c771011e755cd39e83c5cae71d283/telegram%20bot%20token.png)

**Step 5**. "Add agents" to your Telegram inbox.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBLzJrVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--00348d659ebf48f9bd2439403f41307516738cfe/adding%20agents%20to%20a%20chatwoot%20inbox.png)

The inbox setup is complete.

**Step 6**. Go to the Inbox settings page and verify that the inbox name matches the bot username created using BotFather.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBLytrVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--7803d723fd4e53892deba6bbae421217711e0276/telegram%20settings.png)

**Step 7**. Send a message to the Telegram bot. Check Chatwoot Telegram inbox for the new message.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBd0tsVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--38422adfcfadce93d9512267a4d6c4dda7995e7c/telegram%20in%20action%20chatwoot.png)   
 

# FAQs

## Does Chatwoot support Telegram Business Bot accounts?

Yes — support for Telegram Business-mode bots was added in Chatwoot v4.3.0 (18 Jun 2025).

## How to enable Business Bots?

 1. In @BotFather run /business_mode, choose your bot, and confirm.

 2. Create a new Telegram inbox in Chatwoot (Settings → Inboxes → Add Inbox → Telegram) and paste the same bot token.

 3. Chatwoot auto-detects Business Mode and registers the correct webhook.

 4. For best results, keep this Business bot in its own inbox, separate from any standard bot you already use. ￼

## Known issues with Business Bot

 • 24-hour reply window – Telegram only lets the bot (and Chatwoot) reply within 24 hours of the customer’s last message. ￼

 • If a user has previously chatted with the same bot outside Business Mode, replies may appear to come from the bot rather than the Business account;  *creating a dedicated Business bot & inbox avoids this confusion.* 

 • The Telegram Business API is currently less feature-rich than the regular Bot API (e.g., no typing indicators, limited message types). Keep expectations accordingly.
