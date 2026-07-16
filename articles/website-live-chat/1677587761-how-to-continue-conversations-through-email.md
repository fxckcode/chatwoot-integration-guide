# How to continue conversations through email?

Your customers can continue their chat conversations with your agents through email threads. This may be required under the following circumstances.

* No agents are available, and the customer leaves a message in the chat.

* The customer leaves the chat before the agent replies.

For this to work, the contact should have an email address in the Chatwoot CRM.

## Obtaining email addresses of contacts[​](https://www.chatwoot.com/docs/product/channels/live-chat/conversation-continuity#obtaining-email-address-of-contacts "Direct link to heading")

You can prompt/update customer emails into Chatwoot through the following ways.

1. **From Chatwoot SDK**[**​**](https://www.chatwoot.com/docs/product/channels/live-chat/conversation-continuity#1via-chatwoot-sdk "Direct link to heading")

   If customer email is known, you can supply it into chatwoot via the `setUser` method in our [SDK](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/setup).

2. **From pre-chat form**[**​**](https://www.chatwoot.com/docs/product/channels/live-chat/conversation-continuity#2via-prechat-form "Direct link to heading")

   If you enable a mandatory pre-chat form, the conversation starts with a screen as shown below:![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBMzFWVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--581d3070b733c0a9913b888bc873c7bf79dad1fa/email%20collection%20through%20pre%20chat%20form.png)

**3. From Email collect Prompt**[**​**](https://www.chatwoot.com/docs/product/channels/live-chat/conversation-continuity#3via-email-collect-prompt "Direct link to heading")

When the pre-chat form is disabled, and the customer's email is unknown, Chatwoot starts a conversation with an email collect prompt.

*Note*: *When Captain is enabled on an inbox, the email collect prompt is automatically suppressed. Captain will handle conversations directly, even outside business hours. The email collect prompt will only be sent if Captain hands off the conversation to a human agent or if Captain is not configured for the inbox.*

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBM3RWVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--890dbd7daa7e01b886624934ec5f2f159cfc52c1/chatwoot%20prompt%20to%20collect%20emails.png)

## Conversation Continuity[​](https://www.chatwoot.com/docs/product/channels/live-chat/conversation-continuity#conversation-continuity "Direct link to heading")

*Note*: Enable conversation continuity in self-hosted installations with the help of this [guide](https://www.chatwoot.com/docs/self-hosted/configuration/features/email-channel/conversation-continuity).

If the customer's email address is updated through any of the options mentioned above and they leave the chat while the agent has replied, the following happens.

* The customer receives an email thread with a conversation summary. They can reply to that email and continue the conversation.

* The agent receives the customer replies from email in their Chatwoot dashboard, continued over the existing conversation thread.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBM2RWVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--5eaff2c93b0a71dc5042dc62f5f9a3659c71f2f4/conversation%20continuity%20sample.png)

The email icon in the chat bubble indicates that the customer has replied through email.
