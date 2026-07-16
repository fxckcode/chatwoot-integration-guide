# How to enable video calls with Cloudflare RealtimeKit?

Video calling helps your team connect with customers quickly, understand issues clearly, and provide faster support. Chatwoot supports video calls for website live chat conversations through the Cloudflare RealtimeKit integration.

This guide explains how to create the required Cloudflare RealtimeKit credentials, connect them to Chatwoot, and start a video call from a conversation.

> Note: If you previously used the Dyte integration, use Cloudflare RealtimeKit for new setups. Dyte's legacy infrastructure is being sunset after the Cloudflare acquisition.

## Prerequisites

Before you start, make sure you have:

* Access to your Cloudflare account.

* Permission to create a RealtimeKit app in Cloudflare.

* Permission to create Cloudflare API tokens.

* Administrator access to your Chatwoot account.

## How to create a RealtimeKit app in Cloudflare?

**Step 1.** Open the Cloudflare dashboard and go to Realtime -> RealtimeKit.

**Step 2.** Click the "Create app" button.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTE5xblFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--51a81bbedaf78eb5b87b7c7617f0c0e3fc3adc0e/CleanShot%202026-06-18%20at%2012.46.10@2x.png)

\
**Step 3.** Enter a name for the app. For example, you can use "video-support". Click "Create".

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRHhEblFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--3dd16b9ec98a6b1ce13ea89449fb0581de620d36/create-app.png)

\
**Step 4.** After the app is created, copy the RealtimeKit App ID. You will need this value when connecting the integration in Chatwoot.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSHBEblFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--953c57d64fdc09cf98ef6cd22df249d73e9036d2/realtime-id.png)

## How to find your Cloudflare Account ID?

**Step 1.** Go to your Cloudflare account home.

**Step 2.** Click the three-dot menu in the top-right corner.

**Step 3.** Click "Copy account ID".

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSWREblFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--3a9ce95d8a73c8bdd227b2e0d285a025a3547394/account-id.png)

## How to create a Cloudflare API token?

**Step 1.** In Cloudflare, go to My Profile -> API Tokens.

**Step 2.** Click "Create Token".

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSkpEblFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--5b63d3bc28239d459bb59a98c627d775287d80cd/create-token-1.png)

**Step 3.** Under "Custom token", click "Get started".

**Step 4.** Give the token a descriptive name. For example, you can use "video-support".

**Step 5.** Under Permissions, select:

* Scope: Account

* Permission: Realtime

* Access: Admin

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCS05EblFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--104e2d8ada4a8ed4b2d929af29909289810e6e9a/create-token-2.png)

**Step 6.** Under Account Resources, select the Cloudflare account you want to use with Chatwoot. You can select "All accounts" if you want the token to work across all accounts you have access to.

**Step 7.** Review the token summary and click "Create Token".

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTGREblFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--a3678d903d1c8ee7f953d6380de80f15628aae7e/create-token-3.png)

\
**Step 8.** Copy the API token. Cloudflare shows this token only once, so keep it somewhere safe until you add it to Chatwoot.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQVpFblFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--5cdd6e1d3e92af3ec0c9603661fcf10b5fd14987/copy-token-4.png)

## How to set up the RealtimeKit integration in Chatwoot?

**Step 1.** In Chatwoot, go to Settings -> Applications -> Cloudflare RealtimeKit.

**Step 2.** Click "Configure".

**Step 3.** Click "Connect".

**Step 4.** Enter the following values:

* Cloudflare Account ID

* RealtimeKit App ID

* Cloudflare API Token

**Step 5.** Click "Create".

Chatwoot validates the credentials before saving the integration. If any value is incorrect, you will see a specific error for the API token, Account ID, permissions, or RealtimeKit App ID.

Once the credentials are saved, the RealtimeKit integration is ready to use.

## How to video call your customers in Chatwoot?

Once the RealtimeKit integration is enabled, you will see the video calling option in website inbox conversations.

**Step 1.** Open a website inbox conversation.

**Step 2.** Click the video camera icon below the reply editor.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQnRyblFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--9d55787740060e7e8b758d2bd4a73d7973b0ab47/video-call-button.png)

**Step 3.** Chatwoot sends a meeting invitation message to the customer. Click "Click here to join" to enter the call.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRjlFblFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--bd1e312c6314ef045b8ff358b6a1f8d42be043e3/click-to-start-call.png)

**Step 4.** The customer can join the same call from the website live chat widget.

**Step 5.** Once both sides join, the agent and customer can continue the conversation over video or voice.
