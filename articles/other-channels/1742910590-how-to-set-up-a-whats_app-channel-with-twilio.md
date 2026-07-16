# How to Set Up a WhatsApp Channel with Twilio?

Manage your WhatsApp business account conversations through Chatwoot. You have two provider options:

1. WhatsApp Cloud API (preferred way)

2. Twilio

This guide will walk you through the setup process.

## Prerequisites

1. A valid phone number

2. A Twilio account. If you don't have one, create it here: <https://www.twilio.com/en-us/messaging/channels/whatsapp>

## Using Twilio API

There are two ways to use Twilio with Chatwoot:

1. Regular way without messaging service

2. With messaging service

### **Setting Up Twilio Without Messaging Service**

Log into your Twilio account and click on "Create New Account"

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRFNSTkFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--784152d346a96a155ab73a504bb6df54c6e0acb4/t-1.png)

Complete all required fields and finish the account creation process

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRmlSTkFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--7b4d9e0544a6ddfe5f69f79cf0c3f99dcc2b9646/t-2.png)

Copy your Account SID, Auth Token, and phone number. If you haven't added a phone number to your Twilio account yet, do so before proceeding.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSGFSTkFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--e72aadfc84256463109f47ef44c0a1c0fcbbc8fb/t-3.png)

Log into your Chatwoot account, click on Settings > Inbox > Add Inbox and select Whatsapp

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSlNSTkFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--34dd8eb528bdd4535363aa879332db08a2a0ec44/cw-1.png)

Enter your Account SID, Auth Token, and WhatsApp number here

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTHFSTkFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--9b2702ab9f9da5f18ec72567101bf19242fef6c8/t-4.png)

Add agents to manage your WhatsApp inbox

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQStTTkFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--3dd0b29e7fe4edc96f15054775c125bcf708a389/cw-3.png)

Go to Settings > Inbox, select your inbox, click on Configuration, and copy your webhook URL

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQ3FTTkFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b595460c77794a0c3a9198669264102f8f41198d/t-5.png)

Return to your Twilio dashboard

1. Go to Twilio Console → Phone Numbers → Manage → Active Numbers

2. Click on your WhatsApp number.

3. Click Configure

4. Under Messaging, check the field “Webhook (When a message comes in)”.

5. Update the webhook URL.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCT3JyVlFRPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--5a653f228f85ffe8a4bc379bf183bdf83395e328/CleanShot%202026-02-25%20at%2013.30.03@2x.png)

That's it! You're all set to start sending WhatsApp messages through Chatwoot.

### **Setting Up Twilio with a Messaging Service**

Setting up Twilio with a messaging service requires additional steps compared to the regular setup.

Navigate to Messaging > Services and click "Create Messaging Service" button.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCT2VTTkFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--714e74911a5f6e3c8e11826540f83fe30fbf3491/m-1.png)

Fill in all the required fields in the subsequent steps till you reach here. Copy your messaging service ID and click “Save”.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCUHlTTkFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--ea08dfe9f1955053f6d38e8ea4c2ae36a2d21ddf/m-8.png)

Log into your Chatwoot account. When creating an inbox, check the "Use Twilio Message Service" box. Then copy and paste your Account ID, Message Service ID, and Token into the appropriate fields.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQlNUTkFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--d146c4d831b0ebb5fc7fc0766774887c38c6a930/m-10.png)

Go to your Twilio dashboard, navigate to Messaging > Services > Select Service > Integration, and paste your Webhook URL here.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQzNNZHdFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--ffb7d554aa705d75d9434ba766b2626168667dcc/SCR-20250529-pqvo.png)

That's it—you're all set! You can now start sending WhatsApp messages through Chatwoot.

### **FAQ’s**

**What types of WhatsApp templates does Chatwoot support when using Twilio?**

Currently, Chatwoot does not support templates with Twilio.

**I'm using Twilio Studio. Are there additional steps needed to make it work?**

If you use Twilio Studio for a custom conversation flow, updating the webhook URL directly will break your existing integration.

Follow these steps instead:

1. Identify the step in your flow where you want the “**agent handoff”** to happen.

2. Add a “**make http request widget”** as shown below with the given values.

   ![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSTJUTkFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--1e1ddf2affd4b68fb31a3a0971fb7373db88c084/SCR-20250320-cayt.png)

   ![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCS0tUTkFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--3469126ca2b9c752b408006fe8b4b81a6fd10c25/SCR-20250325-tbgg.png)

3. Ensure your flow can handle user responses to agent replies.
