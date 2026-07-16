# How to setup a WhatsApp channel (Manual flow)?

You can manage your WhatsApp business account conversations from Chatwoot. To set it up, you have two options to choose your provider:

1. WhatsApp Cloud API

2. Twilio

We'll explain all the procedures in this guide.

### **Prerequisites**

1. You need a [**Meta Developer Account**](https://developers.facebook.com/) to setup WhatsApp API. If you dont have a developer account already click [**here**](https://business.facebook.com/business/loginpage/) to create one before proceeding

2. A valid phone number

## **Using Whatsapp Cloud API**

[**WhatsApp Cloud API**](https://developers.facebook.com/docs/whatsapp/cloud-api/) is available to all businesses and individual developers. Since it's hosted on Meta's cloud infrastructure, you no longer need to use third-party providers like Twilio, Zendesk, 360Dialog, or MessageBird ([**Business Solution Providers**](https://www.facebook.com/business/partner-directory/search?solution_type=messaging)) to host your WhatsApp Business API.

## **Set up your Business Profile**

Create a professional WhatsApp business profile with your company name, description, and contact information. A well-crafted profile helps customers recognise and trust your brand when they interact with you.

Log into [**https://business.facebook.com**](https://business.facebook.com/) and click the **create portfolio** button in the dropdown menu under Home

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCS0l2TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--72176865da87c663b137ddf7e9fcc96a9895ed79/image.png)

Complete all required fields to set up your business portfolio.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTDB2TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b97272d17bfd653a869efa3463beb3c4e21c2b32/image.png)

Once you have created your business portfolio, it's time to create your Facebook app.

## **Setup your Facebook App**

Log into [**https://developers.facebook.com/**](https://developers.facebook.com/) and click the **Create App** button.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTmt2TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--98e9e282f223ba6c1925a9f6d2a7aed9ef6e558e/image.png)

Complete the required fields

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCUEF2TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--c3a7a0ccb782a47ec460a8bfcf30cdee6d4902c1/app-2.png)

Click "Other" from the options

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQUF3TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--ae78ade6835e127f19708f3c51595393cf0755fb/app-3.png)

Choose "Business" as your app type

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQkV3TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--653dc0f0c7137a07fb8605394443b7ce46ac518b/app-4.png)

Enter your contact email address and choose your business portfolio from the dropdown menu.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQnd3TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--97420cad25fb464103e356169eeea2b8ee2f882e/app-6.png)

## **Add Whatsapp to your app**

After creating your app, you'll be directed to the app dashboard. From there, click **"Add Product"** and choose **WhatsApp** from the available products list.

Click the "Set up" button for WhatsApp

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQ1V3TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--8edbe733b323ed31919bd51914049fa87056c77d/app-7.png)

***Note:** Before proceeding, verify your business with Meta. You'll need to submit documentation for verification, which is required for full API access.*

## **Set Up a Permanent WhatsApp Cloud API Access Token**

You'll need to create a **System User** and generate a permanent token to maintain secure, uninterrupted access.

Log in to your Facebook developer account, select your WhatsApp app, and navigate to the [**Business settings page**](https://business.facebook.com/settings).

Click on "System Users" and add a new system user with the role **Admin**

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRDh3TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--2826694996496e22a3ecf00c12269e7b77a96278/SCR-20250318-tocl.png)

Click the "Add Assets" button, select your app name, choose the "Full Control" option, and click "Assign assets."

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRWt3TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--4513bf38a22f4f420c5894d64dbff22557732be0/assign-assets.png)

Return to the **system users** page, select your newly created system user from the list, and click the "**Generate new token**" button.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRnN3TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--28256cc30c4ee638a5e5127fffaa61b5362eea9e/sys-1.png)

Select your app from the dropdown menu

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCR3N3TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--85305f422e394fb1aef6c146e19f936c6cd092dd/sys-2.png)

Select these three permission levels for your token:

* whatsapp_business_manage_events

* whatsapp_business_management

* whatsapp_business_messaging

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSGt3TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--45b91aa4d3d4c4481a8ce37fc1468fd00386b0fb/sys-3.png)

Copy and save your token

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSUl3TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--9e96636a7551f8073f4c86108ab8fe3f83cfc5bf/sys-4.png)

## **Set Up WhatsApp Cloud API**

To create a new Meta business account, select "**create a business account**" from the dropdown menu. If you already have a business account, you can select it from the existing options. I'm selecting "**create a business account**". Click the ***continue*** button.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSXd3TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--103af678530aa76e8768d7a3d530dd4aef96377e/api-0.png)

Paste your permanent token here

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSnd3TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--403311ae1ce0523a626d6b00dac00e4f74949e6a/api-1.png)

Add your production ready phone number

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCS013TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--cd7b500250f5adc96b90d8e7e3b8cc5bbdfb77a6/api-2.png)*Note*: Meta requires a verified phone number for WhatsApp API setup. You can verify your number using an OTP (one-time password).

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTFF3TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--e3505e8fbd4c9400883212aed134a0e6c6743ef4/api-3.png)

Once you have added and verified your phone number, the next step is configuring a webhook to receive inbound messages.

## **Connecting Your Chatwoot Account**

Let's connect your Chatwoot account with your WhatsApp Cloud API

Copy your WhatsApp Phone Number ID and Business Account ID from this section

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTVl3TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--5817b729bb5f9311f620914e1410c3cba09a988d/phid.png)

Log into your Chatwoot account, go to Settings > Inbox, and select WhatsApp channel

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTTR3TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--34b0791786e1b9185b78563057d4dd6d6d2eeef6/cw-1.png)

Enter your phone number, phone number ID, and business ID from your WhatsApp API setup

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCT1V3TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--36b14c0dff0a29cb3de0a07be4a8fa42f649decb/cw-2.png)

Add team members to your WhatsApp inbox

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCUFl3TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--aff01faf7c0ba58daf722b218a378ebdae62617d/cw-3.png)

Copy the webhook URL and webhook verification token provided here

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQVl4TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--ebc9f3052573b38afdd96995bfd97af6e9ed75cc/cw-4.png)

## **Set Up Your Webhook**

We need to set up the WhatsApp webhook to receive incoming customer messages sent to your business number.

Your callback URL should be in the format of [**https://app.chatwoot.com/webhooks/whatsapp/{phone_number}**](https://app.chatwoot.com/webhooks/whatsapp/%7Bphone_number%7D).

Log into your Facebook developer account and navigate to WhatsApp > Configuration

Paste your Chatwoot webhook URL and verification token here, then click "Verify and Save"

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQmN4TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--3802889ac4ce26cd2264b6dab4267fd1cb6afe53/hk-1.png)

Set up webhook permissions by subscribing to messages

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQ1V4TlFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--a8d5c4c957aa29875247a3b135eb2acf945fddcc/hk-2.png)

That's it—you're all done! You can now start sending WhatsApp messages through Chatwoot.

### **FAQ’s**

**How to configure multiple numbers under a single Facebook app?**

Facebook App allows configuring only a single Webhook endpoint. So create Inboxes in Chatwoot for all the numbers as required. You will need to configure the Webhook URL provided for only one of these inboxes in the Facebook app for all the other inboxes to work.

**What type of Whatsapp templates are supported by Chatwoot ?**

Please check the [**doc**](https://www.chatwoot.com/hc/user-guide/articles/1754940076-whatsapp-templates) for more details about templates.

**What are the supported media types?**

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRHZuSWdJPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--469bfec94ea6ac0381da7d5223e83312dbaf5ca9/image.png)
