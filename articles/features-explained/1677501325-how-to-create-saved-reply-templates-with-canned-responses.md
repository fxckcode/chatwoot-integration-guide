# How to create saved reply templates 
with Canned Responses?

Canned responses let you save frequently sent messages as templates. Whenever you need to use a saved reply in a conversation, you can access canned responses by typing **`/`** followed by a shortcode.

You can use canned responses to save replies to frequently asked questions, which will help reduce an agent's response time and productivity. All canned responses are available for all agents in the account.

P.S. We have curated a bunch of editable, templated replies for you to create your Canned Responses with. [**Check it out**](https://www.chatwoot.com/tools/canned-responses-library).

## How to create a canned response?

Any agent/admin in the account can create/modify a canned response. To add a new canned response, follow the steps described below.

**Step 1.** From the sidebar, click on **Settings → Canned Responses → Add canned response**. By default, there are no canned responses available in the account.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRmJaSXdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--513d61a4fd4ce7ae7ce06ea4d36b3b80d4a85283/canned-responses.jpg)

**Step 2.** A modal will open up, as shown below.

\
![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSXJaSXdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--db2bcc712715595d0cc2199c74c5bcad0770a6e4/add-canned-response.jpg)

The fields shown in the modal are described below.

1. **Short Code**

   Write a short code you can easily remember later to use. The minimum length required is 2 characters. Every shortcode is unique.

2. **Content**

   Type in the message you want to save as a template.

Once you enter the details, click the **Submit** button. If the request is successful, a message "Canned Response added successfully" will be displayed.

## How to modify or delete a canned response?

**Step 1.** Open the list of your canned responses from **Settings → Canned Responses**. Locate the canned response you want to edit. Click the Edit button (pencil icon) if you want to edit it. Click the delete button (red cross icon) if you want to delete it.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekU2dXc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--986a446b2460cf306ed28162bafb0f4ddf41b327/edit-delete-canned.png)

**Step 2.** If you are editing the canned response, you will see a modal with prefilled information. You can edit both the shortcode and the message. Click on **Submit** to save the changes. Click on **Cancel** if you want to discard the changes.

\
![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTExaSXdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--c7c18f2aa45a4301050bb3d7e2d1c9a9bc78d67c/edit-canned-response.jpg)

## How to use a canned response in a conversation?

To access canned responses while you chat with a customer, enter `/` in the text editor. This will display a list of all the canned responses. You can choose from the list or simply type in the shortcode if you remember it. Then, press the `Enter` key, and your text editor will be populated with the reply.

\
![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTmpaSXdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--f63b5c4e39cfd24a2886be1b0203b9e02c0fb73b/canned-responses.gif)

## Template variables

Canned responses support placeholder variables that auto-fill from the conversation context. Wrap them in double curly braces.

### Contact variables

* `{{contact.id}}`

* `{{contact.name}}`

* `{{contact.first_name}}`

* `{{contact.last_name}}`

* `{{contact.email}}`

* `{{contact.phone}}`

### Agent variables (the person sending the message — you)

* `{{agent.name}}`

* `{{agent.first_name}}`

* `{{agent.last_name}}`

* `{{agent.email}}`

### Inbox / conversation variables

* `{{inbox.name}}`

* `{{inbox.id}}`

* `{{conversation.id}}`

### Custom attribute variables

* `{{contact.custom_attribute.<key>}}` — any contact custom attribute by key

* `{{conversation.custom_attribute.<key>}}` — any conversation custom attribute by key

### Example template

```
Hi {{contact.first_name}},

Thanks for reaching out about your {{contact.custom_attribute.plan}} plan.

I'm {{agent.first_name}} from the {{inbox.name}} team — I'll take a look

at this and get back to you within the hour.

Best,

{{agent.first_name}}
```

If a variable has no value (e.g. the contact has no first name on record), the placeholder is replaced with a blank — keep your fallbacks readable.

## Frequently asked questions

**Can I edit the inserted text before sending?**

Yes — the canned response just fills the reply box. You can edit, append, or delete anything before clicking Send.

**Can I include images in a canned response?**

Inline images aren't part of the canned response itself, but you can attach images to the reply after the canned text fills in. Alternatively, you can use macros if you need image support.

**Are canned responses synced across channels?**

Yes — the same response works in any channel. Markdown rendering depends on the channel (rich rendering on Website/Email, plain text on SMS).
