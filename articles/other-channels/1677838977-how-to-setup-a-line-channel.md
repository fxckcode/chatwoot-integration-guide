# How to setup a Line channel?

**Step 1**. Go to Settings → Inboxes → “Add Inbox”.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBd3FsVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b8de64b959037f719822133fad377bbaae3b5235/adding%20an%20inbox%20in%20chatwoot.png)

**Step 2.** Click on the "Line" icon.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBeGFsVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--cd955d11f48f40cdf3e5756d0c3eeaa2905968d0/line%20inbox%20in%20chatwoot.png)

**Step 3.** Go to the [Line Developer Console](https://developers.line.biz/console) and create a Line account.

**Step 4**. Create a "Provider" in the developer console. Create a new "Messaging API" channel(Bot) under the provider.

**Step 5.** Fill up the below fields from the Line developer console (Messaging API Channel) and click "Create LINE Channel".

1. Channel Name

2. LINE Channel ID

3. LINE Channel Secret

4. LINE Channel Token

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBeGlsVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--40489471407baac92ca726c877646f619e641624/line%20inbox%20settings.png)

**Step 6**. "Add agents" to your Line inbox.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBeHFsVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--d685f6bc6e56691e370ffa77e0d6a502c13b1315/adding%20agents%20to%20a%20chatwoot%20inbox.png)

The inbox setup is complete.

**Step 7.** Go to the "Messaging API" channel in the developer console and configure the webhook.

1. Verify Chatwoot webhook URL

2. Enable "Use webhook"

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBeHVsVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--360722da274cb96160172a3735d48f951b4d2d60/line%20webhook%20settings.png)

**Step 8**. Test your new Line inbox. Send a message to the Line bot. Check Chatwoot Line inbox for the new message.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBeHlsVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--cf08993a8cbbbe2256c2896d85ed32fd58e593c0/testing%20line.png)
