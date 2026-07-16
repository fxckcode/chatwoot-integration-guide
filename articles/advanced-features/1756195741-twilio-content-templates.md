# Twilio content templates

Twilio Content Templates allow you to send pre-approved WhatsApp message templates through your Twilio WhatsApp Business channels in Chatwoot. These templates enable you to initiate conversations and send structured messages that comply with WhatsApp's messaging policies.

## **Template Types Supported**

**Text Templates**

* Simple text messages with optional variables

* Support for up to 100 variables per template using `{{1}}`, `{{2}}` format

* Multi-language support

**Media Templates**

* **Image Templates**: Text with image headers (JPEG/PNG, max 5MB)

* **Video Templates**: Text with video headers (MP4/3GPP, max 16MB)

* **Document Templates**: Text with document attachments (PDF/Office formats, max 100MB)

* Support for dynamic media URLs with variables

**Quick Reply Templates**

* Interactive button responses handled by WhatsApp

* Simple button actions for common responses

* Support for multiple language variants

**Call-to-Action Templates**

* **URL Button Templates**: Send messages with clickable action buttons

* **Variable Support**: Both message text and button parameters can include variables

* **Action Types**: URL buttons for payments, bookings, websites, etc.

## **Prerequisites**

Before using Twilio Content Templates:

1. **Twilio Account**: Active Twilio account with WhatsApp Business API access

2. **Approved Templates**: Templates created and approved in Twilio Console

3. **Chatwoot Integration**: Twilio WhatsApp channel configured in Chatwoot

4. **WhatsApp Business Account**: Verified WhatsApp Business profile

## **Setting Up Templates**

1. Log into your [Twilio Console](https://console.twilio.com/)

2. Navigate to **Messaging** → **Content Template Builder**

3. Click **Create new template**

4. Choose your template type: **Text**: For simple text messages, **Media**: For images, videos, or documents,  **Quick Reply**: For interactive buttons

5. Configure the template based on the purpose.

6. Submit template for WhatsApp approval

7. Wait for approval (5 minutes to 24 hours)

8. Approved templates receive a ContentSid

9. Templates are now ready for use in Chatwoot

## **Syncing Templates to Chatwoot**

**Automatic Sync via API**

Templates are automatically synced when you:

1. Open the content templates modal in a conversation

2. Create a new conversation with a Twilio WhatsApp channel

**Manual Sync**

For inbox administrators:

1. Go to **Settings** → **Inboxes**

2. Select your Twilio WhatsApp inbox

3. Click **Sync Templates** button

4. Wait for sync completion notification

## **Using Templates in Conversations**

#### **Step 1: Access template options**

Open any conversation with a WhatsApp contact, Click on the **template icon** in the message composer, Select **"WhatsApp Templates"** from the dropdown menu

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTnAxRXdJPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--859d1249d1c6a48c60b489dbcd8e64c9cb051213/CleanShot%202025-08-26%20at%2013.49.16@2x.png)

#### **Step 2: Choose your template**

Browse through your approved templates, Use the search bar to find specific templates quickly

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTzExRXdJPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--c4a753fd824fadbe3a6f3bb225fbdd38c7452d56/CleanShot%202025-08-26%20at%2013.51.19@2x.png)

#### **Step 3: Customize your message**

Depending on your template type, you may need to fill in:

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCUFIxRXdJPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--75e325a080c3749165473b87370618b8246c0a4e/CleanShot%202025-08-26%20at%2013.51.56@2x.png)

## **Best Practices**

**Template Design**

* Keep messages concise and clear

* Use variables for personalization

* Ensure media files are optimized and accessible

* Test templates before approval submission

**Variable Usage**

* Use descriptive variable names in Twilio Console

* Provide clear examples for approval

* Keep variable count reasonable (under 10 for best UX)

**Media Guidelines**

* Host media files on reliable, fast servers

* Use HTTPS URLs for all media

* Optimize file sizes for faster delivery

* Include fallback text for media templates

**Compliance**

* Follow WhatsApp Business Policy guidelines

* Ensure templates serve legitimate business purposes

* Respect user privacy and consent

* Monitor template performance and approval status

## **Troubleshooting**

**Common Issues**

**Template Not Appearing**

* **Cause**: Template not approved by WhatsApp

* **Solution**: Check approval status in Twilio Console

**Template Sync Failed**

* **Cause**: API connection issues or invalid credentials

* **Solution**: Verify Twilio credentials and retry sync

**Media Not Loading**

* **Cause**: Media URL not accessible or wrong format

* **Solutions**: Verify URL is publicly accessible, Check file format and size limits, Ensure HTTPS protocol

**Variables Not Working**

* **Cause**: Incorrect variable format or missing values

* **Solutions**: Use correct `{{1}}`, `{{2}}` format in Twilio, Fill all required variables in Chatwoot, Check variable count matches template

## **Error Messages**

**"Template not found"**

* Template not synced to Chatwoot

* Run manual sync or check template approval

**"Media file too large"**

* File exceeds WhatsApp limits

* Compress file or use different format

**"Invalid template parameters"**

* Missing or incorrect variable values

* Review and complete all required fields

## **Template Examples**

**Basic Text Template**

```

Name: welcome_message

Content: "Welcome to {{1}}! We're excited to help you with {{2}}."

Variables: Company name, Service type
```

**Product Showcase (Media Template)**

```

Name: product_launch

Media: Product image

Content: "🎉 New arrival! {{1}} is now available for {{2}}. Limited time offer!"

Variables: Product name, Price
```

**Order Confirmation (Text Template)**

```

Name: order_confirmed

Content: "Hi {{1}}! Your order {{2}} has been confirmed. Delivery expected: {{3}}."

Variables: Customer name, Order ID, Delivery date
```

**Quick Reply Template**

```

Name: support_options

Content: "How can we help you today?"

Buttons: "Technical Support", "Billing", "General Info"
```

## **Limitations**

**Current Limitations**

* Templates not supported in campaigns (coming in future updates)

* List picker templates 

* Catalog templates

* Carousel templates

**Template Limits**

* Maximum 100 variables per template

* Media files must be publicly accessible

* Templates require WhatsApp approval

* Sequential parameter numbering required

## **Support**

For additional help:

* Check [Twilio WhatsApp Documentation](https://www.twilio.com/docs/whatsapp)

* Review [WhatsApp Business Platform Guidelines](https://developers.facebook.com/docs/whatsapp/business-platform)

* Contact your system administrator for technical issues

* Refer to Chatwoot documentation for general platform guidanc
