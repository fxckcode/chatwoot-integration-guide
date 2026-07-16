# How to migrate from Freshdesk to Chatwoot?

If you're currently using Freshdesk and want to switch to Chatwoot, this guide will walk you through the step-by-step process of migrating your conversations, contacts, live chat widget, and setting up Chatwoot. This is a very quick process; let’s dive in.

## Before you begin

Before setting up Chatwoot, there are two essential preliminary tasks to complete in order to smoothly remove Freshdesk from your ecosystem.

### **Step 1.** Remove the Freshdesk chat widget

To start, please make sure to uninstall the existing live chat code that you would have previously integrated for enabling the Freshdesk live chat widget on your website.

### **Step 2.** Export contacts

Next, visit the ‘Contacts’ tab in your Freshdesk account. Check the box next to 'Select all' to ensure that all of your contacts are selected. Then click the 'Export' button. Follow the on-screen instructions to complete your export and save it to your system.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBNEtqY3c9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--7acc8f7e4ffcf26fee375ee0ec394d92dba4934c/freshdesk-contacts-export.jpg)

## Migrating to Chatwoot

### **Step 3.** Sign up

Create an account in Chatwoot, using [this guide](https://www.chatwoot.com/hc/chatwoot-user-guide-cloud-version/articles/1677242820-create-your-chatwoot-account).

### **Step 4.** Migrate the live chat widget

Create a live chat inbox in Chatwoot, using [this guide](https://www.chatwoot.com/hc/chatwoot-user-guide-cloud-version/en/categories/website-live-chat). At the end of the setup, you will find the live chat code snippet to be pasted into your website’s codebase. Complete this step, ensuring that you have already removed the live chat code snippet for Freshdesk's live chat widget, as mentioned in Step 1.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBL0tqY3c9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--7391ca4becc3bbf17385a56f8bde31b5a63ba31c/chatwoot-messenger-snippet.jpg)

### **Step 5.** Migrate contacts

Open the ‘Contacts’ tab in Chatwoot, press the Import button.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBL1NqY3c9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--0d7a361585897f5a8f917d32f808d32603bd0b7b/importing-contacts-in-chatwoot.jpg)

Next, follow the on-screen instructions to upload the Contacts file exported from Freshdesk, in a `csv` format. Once your upload is completed, all of your contacts will be successfully synced in Chatwoot.

### **Step 6.** Migrate conversations

For importing your existing conversations from Freshdesk to Chatwoot, use [this API](https://www.chatwoot.com/developers/api/#tag/Conversations/operation/newConversation).

### **Step 7.** Make Chatwoot your own

You are all set to use Chatwoot, congratulations! We recommend the following steps to begin making the best of Chatwoot:

[Chatwoot 101 tutorials](https://app.chatwoot.com/hc/chatwoot-user-guide-cloud-version/en/categories/chatwoot-101): A comprehensive guide to learn the basics of Chatwoot within minutes.

[Omnichannel inbox](https://app.chatwoot.com/hc/chatwoot-user-guide-cloud-version/en/categories/other-channels): A helping hand to setting up your omnichannel customer service on Chatwoot.

A few [best practices](https://app.chatwoot.com/hc/chatwoot-user-guide-cloud-version/en/categories/best-practices) to make your workflow smooth as butter on Chatwoot.

For everything else, hit us up on `hello@chatwoot.com`, and don't forget to share your feedback with us. Happy chatting!
