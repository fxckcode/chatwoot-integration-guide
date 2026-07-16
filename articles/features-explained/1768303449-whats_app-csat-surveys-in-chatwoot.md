# WhatsApp CSAT Surveys using Templates

Customer Satisfaction (CSAT) surveys help you understand how happy customers are with the support they receive on WhatsApp. Chatwoot now supports **CSAT surveys via WhatsApp message templates**, so surveys can be sent reliably even after the 24-hour WhatsApp messaging window.

When a conversation is resolved, Chatwoot can automatically send a short survey to the customer on WhatsApp asking them to rate their experience.

The survey message contains:

* A short text message (for example: asking for feedback)

* A button that opens the CSAT rating page

Customers tap the button and submit their rating in just a few seconds.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSTVwWGdNPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--a41171df0f5295a073a7ae1a725899bd30c9718f/CleanShot%202026-01-13%20at%2015.20.03@2x%201%20(2).png)

## Why does WhatsApp require a template?

WhatsApp only allows free‑form messages within 24 hours of a customer’s last message.

There is a high chance that CSAT surveys are usually sent **after a conversation ends**, they must be sent using a **WhatsApp message template** approved by WhatsApp.

Chatwoot takes care of this automatically:

* A template is created for your CSAT message

* The template is sent to WhatsApp for approval

* Once approved, it is used to send CSAT surveys

You don’t need to manually create or manage templates.

> You can use CSAT Template surveys if You are using a WhatsApp Cloud  or Whastapp Twilio inbox in Chatwoot

## How to enable CSAT for a WhatsApp inbox

Follow these steps to turn on CSAT surveys.

### Step 1: Open your WhatsApp inbox settings

1. Go to **Settings → Inboxes**

2. Select your **WhatsApp inbox**

3. Open the **CSAT** tab

### Step 2: Enable CSAT

Turn on the **Enable CSAT** toggle.

Once enabled, Chatwoot will prepare a WhatsApp template for your survey.

### Step 3: Customize the survey message

Fill in the following fields:

* **Message:** The text customers will see before rating.

* **Button text** The label shown on the button.

* **Language:** Choose the language for your WhatsApp audience.

A live preview is shown on the right so you can see how it will look on WhatsApp.

\
![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCT1krWGdNPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--73f2b8ab77e225efbbf517926630032ee0b23660/CleanShot%202026-01-13%20at%2015.04.54@2x%201.png)

## Template approval status

After saving, you may see one of these statuses:

* **Pending approval**\
  WhatsApp is reviewing your CSAT template. This can take some time.

* **Approved**\
  The template is approved and CSAT surveys will be sent automatically.

* **Rejected**\
  WhatsApp rejected the template. You can update the message and try again.

Once approved, no further action is required.

## What happens when a conversation is resolved?

When a conversation ends:

1. Chatwoot checks if the conversation matches your survey rules

2. If yes, the CSAT survey is sent using the approved WhatsApp template

3. The customer taps the button and submits their rating

Surveys are sent **only once per conversation**.

## Updating your CSAT message later

WhatsApp does **not allow editing** an approved template.

So when you change any of the following:

* Survey message text

* Button text

* Language

Chatwoot will show a confirmation message explaining that:

* The old template will be replaced

* A new template will be created and sent for approval

After approval, the new template will be used automatically.

## Good practices for WhatsApp CSAT

* Keep the message short and friendly

* Use clear button text like “Rate now” or “Give feedback”

* Send surveys only for meaningful conversations using labels

* Avoid changing templates too frequently to reduce approval delays
