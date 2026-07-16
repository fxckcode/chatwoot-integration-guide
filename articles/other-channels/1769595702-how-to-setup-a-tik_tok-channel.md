# How to setup a TikTok channel?           

If you are using a self-hosted Chatwoot installation, please set up your TikTok app as described in is this [guide](https://developers.chatwoot.com/self-hosted/configuration/features/integrations/tiktok).

For the cloud version of Chatwoot, please follow this guide.

## Prerequisites

Before setting up the TikTok channel, ensure the following:

1. You have a **TikTok Business Account** registered in an eligible region.

2. Your TikTok Business Account is set to **accept direct messages from everyone**. Otherwise, you will need to manually accept messages in the TikTok app. Learn how to update your [message settings](https://ads.tiktok.com/help/article/how-to-update-your-tiktok-direct-message-permission-for-tiktok-messaging-ads?lang=en)

## Setting Up the TikTok Channel

### **Step 1: Navigate to Inboxes**

Go to **Settings** > **Inboxes** and click **Add Inbox**.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQVp3ckFNPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--0d0a8a83c80966fe34ba08d8645527078e030f7d/inbox-list%201.png)

\
Select **TikTok** from the list of available channels.

### **Step 2: Connect Your TikTok Account**

### Click **Continue with TikTok** to begin the authentication process.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQWR6ckFNPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--3ab38abf2f8a7be77e532ee5954bf5f8d9dd6647/add-channel%201.png)

### **Step 4: Authorize Chatwoot**

\
You will be redirected to TikTok. Review the requested permissions and click **Continue** to authorize Chatwoot to access your TikTok Business Account.

\
![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRngzckFNPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--f254f5a505de5834a432910c999785261623defe/tiktok.png)

### Step 5: Add Agents

\
After authorization, you will be redirected back to Chatwoot. Add agents to the TikTok inbox so they can view and respond to messages.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSTV0ckFNPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--e918d75da1afe3de6bcdbb5649f53a1904341e8c/add-agent.png)\
\
Your TikTok channel is now connected. Incoming TikTok direct messages will appear in your Chatwoot dashboard.

## Messaging Limitations

* Customers must initiate the conversation, businesses cannot message first.

* Agents can send up to **10 messages** before the customer replies. Once the customer replies, messaging is unlimited.

* The reply window is **48 hours** from the customer's last message.

* Only **text**, **image**, and **post share** messages are currently supported due to limitations in the TikTok Business Messaging API.

* Messages sent directly from the TikTok app will be synced into Chatwoot.

* Messages received in unsupported formats (e.g., audio, stickers) will appear as "This message is unsupported. You can view this message on the TikTok app."

## **FAQ’s**

### Why can't I send media messages to some TikTok users?

This happens due to TikTok's restrictions. Some regions do not allow sending or receiving images, and in other cases, the user's account may be flagged by TikTok.

### Which countries support TikTok Business Messaging?

TikTok Business Messaging API is not currently available in the EEA, Switzerland, or the UK. Messaging features may be limited or unavailable for users in these regions.  For the latest supported regions and restrictions, please refer to TikTok’s official [documentation](https://business-api.tiktok.com/portal/docs/business-messaging-api/v1.3).

## **Availability**

TikTok is available on both Cloud and Self-hosted plans.
