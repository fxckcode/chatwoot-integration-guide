# Whatsapp templates

WhatsApp templates are pre-approved message formats that allow you to initiate conversations with your customers. They're essential for sending promotional messages, order updates, and support notifications through WhatsApp Business Platform.

**Note:** WhatsApp templates are currently supported only for WhatsApp Cloud inboxes.

## **What are WhatsApp Templates?**

WhatsApp templates are structured messages that must be approved by WhatsApp before you can send them to customers. They help ensure compliance with WhatsApp's messaging policies while enabling you to send professional, consistent communications.

Templates can include:

* **Text messages** with personalized variables

* **Images, videos, or documents** as headers

* **Action buttons** for quick customer responses

* **Call-to-action buttons** that link to websites or phone numbers

## **Template Categories**

WhatsApp organizes templates into different categories based on their purpose:

* **Utility** - Transactional messages like order confirmations and receipts

* **Marketing** - Promotional content and special offers

* **Shipping Update** - Delivery and package status updates

* **Ticket Update** - Support case notifications

* **Issue Resolution** - Customer service follow-ups

## **What is not supported**

### **Authentication templates**

* **AUTHENTICATION** templates with OTP codes and verification messages

* **Auto-population** of button parameters with OTP values

* **OTP validation** and expiry time handling

### **Interactive components**

* **LIST** templates with selectable options

* **PRODUCT** templates with catalog integration

* **CATALOG** templates for product browsing

* **Multi-select** components

### **Call permission components**

* **CALL_PERMISSION_REQUEST** templates requiring WhatsApp calling API enabled

* **Call permission** buttons and interactive call components

### **Location components**

* **LOCATION** headers with map coordinates

* **Address** parameters with latitude/longitude

* **Location-based** templates

### **Advanced features**

* **Rich text formatting** in template creation (preserved in sending)

* **Carousel** templates with multiple cards

* **Form** components for data collection

* **Payment** integration templates

* **Flow** templates with conditional logic

## **Legacy vs Enhanced templates**

Chatwoot supports two template formats to ensure compatibility with all your existing templates:

### **Legacy templates**

These are traditional templates that use simple text variables. They work with:

* Basic text messages

* Simple variable substitution (like inserting a customer name)

* Straightforward button interactions

**Legacy format example:**

```
{
  "parameters": ["John Doe", "12345", "2025-01-15"]
}
```

**⚠️ Important:** Legacy template support will be discontinued in the v4.7. We recommend migrating to enhanced templates to ensure continued functionality.

### **Enhanced templates**

The new enhanced format provides more sophisticated features:

* **Media support** - Send images, videos, and documents

* **Advanced variables** - More flexible text personalization

* **Interactive buttons** - URL buttons with dynamic links, copy codes, and quick replies

* **Better validation** - Real-time checking of your template parameters

**Enhanced format example:**

```
{
  "body": {
    "1": "John Doe",
    "2": "12345",
    "3": "2025-01-15"
  },
  "header": {
    "media_url": "https://example.com/image.jpg",
    "media_type": "image"
  },
  "buttons": [
    {
      "type": "url",
      "parameter": "track123"
    }
  ]
}
```

**Note:** All your existing legacy templates continue to work for now, but you should plan to transition to enhanced templates. Enhanced features are automatically available when you use supported template types.

Please check this [API](https://developers.chatwoot.com/api-reference/messages/create-new-message) to know about the request formats.

## **How to create WhatsApp templates**

Currently, WhatsApp templates must be created through **WhatsApp Business Manager**:

1. **Access WhatsApp business manager** - Go to [business.facebook.com](http://business.facebook.com)

2. **Navigate to templates** - Find the "Account tools" section and select "Message templates"

3. **Create new template** - Click "Create template" and choose your template type

4. **Design your template** - Add header, body, footer, and buttons as needed

5. **Submit for approval** - WhatsApp will review your template (this can take up to 24 hours)

6. **Sync to Chatwoot** - Once approved, templates will automatically appear or you can manually sync templates via inbox in Chatwoot

**🚀 Coming Soon:** We're planning to add template creation directly within the Chatwoot interface in a future release, making it easier to design and manage your templates without leaving Chatwoot.

## **How to send WhatsApp templates**

WhatsApp templates can be sent in two ways:

* **Individual conversations** - Send templates to specific customers during conversations

* **Campaigns** - Send templates to multiple customers at once using Chatwoot's campaign feature

### **Sending templates in conversations**

#### **Step 1: Access template options**

Open any conversation with a WhatsApp contact, Click on the **template icon** in the message composer, Select **"WhatsApp Templates"** from the dropdown menu

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRHdUOUFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--257425a35b90c4a3b936f58c29eee946763157ef/CleanShot%202025-08-12%20at%2001.12.20@2x%201.png)

#### **Step 2: Choose your template**

Browse through your approved templates, Use the search bar to find specific templates quickly

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQVVVOUFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--4da9876c768ccdb2ef56825c4634e68e7c62542e/CleanShot%202025-08-12%20at%2001.17.34@2x%201.png)

#### **Step 3: Customize your message**

Depending on your template type, you may need to fill in:

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTTRUOUFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--0c7ab1c26180341571b6a4bcdfc63078ee41c710/CleanShot%202025-08-12%20at%2001.16.32@2x%201.png)

**For text templates:**

* Customer name, order number, or other personalized information

* Any variable fields marked with {{1}}, {{2}}, etc.

**For media templates:**

* **Image/Video URL** - Provide a direct link to your media file

* **Document URL** - Link to PDFs, Word documents, or other files

* **Media must be publicly accessible** (no login required)

**For Button templates:**

* **URL parameters** - Dynamic links for call-to-action buttons

* **Copy codes** - Discount codes or referral codes

* **Phone numbers** - For click-to-call buttons

#### **Step 4: Preview and send**

1. Review your message in the preview panel

2. Check that all variables are filled correctly

3. Verify media URLs are working (if applicable)

4. Click **"Send Template"** to deliver your message

### **Sending templates via Campaigns**

For sending templates to multiple customers at once:

Go to Whatsapp **Campaigns** in your Chatwoot dashboard and create a new campaign and select **WhatsApp** as the channel

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRTRVOUFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--dcaa88c461718dae1746763a0d25b3538c8f16c5/CleanShot%202025-08-12%20at%2001.19.07@2x%201.png)

Choose your WhatsApp template from the available options and configure your audience and template parameters

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRlRoOUFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--d702cb8e1080e0e96d647876eeaf048f7990c1bd/og-help-center%20(1).png)

**Note:** Campaign functionality allows you to reach multiple customers efficiently with the same template message.

## **Frequently Asked Questions (FAQ)**

### **General Questions**

**Why can't I see all my WhatsApp templates in Chatwoot?**

Only templates that are approved by WhatsApp and supported by Chatwoot will appear. Unsupported template types (like authentication templates with OTP codes) are automatically filtered out.

**How long does it take for new templates to appear in Chatwoot?**

Templates typically sync automatically after some time and also you can update it manually from inbox settings.

**Can I edit templates directly in Chatwoot?**

No, templates must be created and edited in WhatsApp Business Manager. Chatwoot is used only for sending approved templates.

**Why do I need to provide URLs for images and videos?**

WhatsApp requires media files to be hosted online and publicly accessible. You cannot upload files directly - you must provide working URLs to your media content.

**Can I use the same template for different customers?**

Yes! Templates are designed to be reused. Just fill in different customer information each time you send the template.

### **Troubleshooting**

**My template fails to send. What should I check?**

Common issues include:

* **Missing variables** - Ensure all required fields are filled

* **Broken media URLs** - Verify your image/video/document links work

* **File size too large** - Check that media files meet WhatsApp size limits

* **Template not approved** - Confirm template status in WhatsApp Business Manager

**Why can't customers see my images/videos?**

This usually means:

* The URL is not publicly accessible

* The file format is not supported

* The file is too large

* The hosting server is down or requires authentication

**My URL buttons don't work correctly. How do I fix this?**

For templates with dynamic URL buttons, there are known issues with certain template configurations. Try using static URLs instead of dynamic parameters for more reliable functionality.

**Can I send templates to customers who haven't messaged me first?**

Yes, but only for certain template categories:

* **Utility templates** can be sent anytime for transactional purposes

* **Marketing templates** require customer opt-in and have specific sending windows

* Always follow WhatsApp's compliance guidelines for your region

### **Media and Files**

**What file types can I use in templates?**

Supported formats include:

* **Images:** JPEG, PNG (under 5MB)

* **Videos:** MP4, 3GPP (under 16MB)

* **Documents:** PDF, DOC, DOCX, XLS, XLSX, PPT, PPTX, TXT (under 100MB)

### **Compliance and limits**

**How many templates can I send per day?**

This depends on your WhatsApp Business account limits and message quotas. Contact WhatsApp support for specific limits on your account.

**Are there restrictions on when I can send marketing templates?**

Yes, marketing templates have specific sending windows and require customer opt-in. Check WhatsApp's current policies for your region and business type.

**What happens if I send too many messages?**

WhatsApp monitors message quality and delivery rates. Sending too many unsuccessful or unwanted messages can impact your account's message limits and template approval rates.

## **Need more help?**

If you're experiencing issues not covered in this guide:

1. **Check template status** in WhatsApp Business Manager

2. **Verify media URLs** are working and publicly accessible

3. **Test with sample data** before sending to customers

4. **Contact your Chatwoot administrator** for account-specific issues

5. **Review WhatsApp's template policies** for compliance questions

Remember that WhatsApp templates are a powerful tool for customer communication when used correctly. Focus on providing value to your customers with relevant, timely messages that respect their preferences.PI
