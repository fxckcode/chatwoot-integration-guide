# How to answer conversations from Slack?

If your company/account/project uses Slack as a communication medium, you can integrate Slack with Chatwoot to manage all the inbox conversations in your slack workspace.

To start the quick setup, follow the steps explained below. If you are using a self-hosted Chatwoot instance, please follow this [guide](https://www.chatwoot.com/docs/self-hosted/configuration/features/integrations/slack-integration-setup).

## How to integrate Slack with Chatwoot?

**Step 1.** Go to **Settings -> Integrations -> Slack -> Connect**.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBd3FVVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--4af1c0e0b2dd65f90f95bb0059d51bf5308f108e/slack%20integration%20in%20chatwoot.png)

**Step 2.** Enter your Slack workspace URL as prompted.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBdzJVVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--384175f15319486e93b8f44b9854463c4ffe76db/slack.png)

**Step 3.** Review the permissions and allow the Chatwoot app to access your Slack workspace.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBdytVVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--2b3cedae0b5c28758d95bbba19b0e5532f2267aa/chatwoot%20slack%20permissions.png)

**Step 4.** You will be redirected to the setup screen, where you will be able to see a list of your Slack channels (public and private). (For private channels, see the section below) You need to select a channel of your choice from the dropdown menu where you want to receive your Chatwoot conversations.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBM1p4Ync9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--652c6cdbfa4f63dedc68c2ccc085f60a8a33442f/selecting%20slack%20channel.png)

Click the Update button. Now, the integration is complete.

### Important note

If you have connected Slack before September 2023, you would not have had the option of selecting a specific Slack channel to manage your conversations from. If you would like to change that and select a specific channel of your choice, you will need to delete your existing Slack integration from the Chatwoot app and connect it again.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBNkJ4Ync9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--d8290f6d20adefaddcb9ee7e40d155b7cf5938ac/deleting%20slack%20integration.png)

### FAQ

**Q. I am replying to a message, but it's not showing up in the Chatwoot inbox.**

A: When you reply to the message, reply under the same thread. Each thread represents a separate conversation, so to show your reply to the same message, you should reply under the thread. We use thread ID to verify the separate conversation.

## Supported features

### Answer from your agent profile

When you reply to a conversation from Slack, the customer receives the reply from your Agent profile in Chatwoot.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekNVVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--c272221664295b81ffef27303bd4aa1ef0c5704e/answering%20chatwoot%20chat%20from%20slack.png)

### Create private notes from Slack

You can create a [private note](https://www.chatwoot.com/features/private-notes) in Chatwoot from Slack. If you prefix a message with "note:", it converts into a private note and notifies any tagged agents. Here is an example:

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBekdVVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--ef9175ae7809446c8730fdc7d1debe9b820bad47/private%20notes%20from%20slack.png)

## How to add Chatwoot to private channels?

Chatwoot won’t be added to your private Slack channels by default. You’ll need to add it manually. Here’s how to do it:

**Step 1:**

After you authenticate with Slack, you’ll be redirected to a page in Chatwoot where you can select the required channel.

**Step 2:** Go to Slack and open the private channel you want to connect. Click on the user icons at the top of the channel. Go to **Integrations** → **Add apps**.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRUltaVFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--f7264db3bf7f6337ad028a2baf6963cdff54ea50/private-channel.jpg)  
**Step 3:** Search for **Chatwoot**. You’ll see the Chatwoot app in the list. 

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRThtaVFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b075dcb9358c244ec416f8182612834706b9c496/search-chatwoot.png)

**Step 4:** Click on **Chatwoot** to add it to the private channel. You’ll see a confirmation message saying that Chatwoot has been added.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRjBtaVFFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--cae35cf393995d6f70644942787593e2e24e9f9a/Screenshot%202025-06-11%20at%2010.52.33%E2%80%AFPM.png)  
**Step 5:** Go back to the Chatwoot app and refresh the page. The channel should now appear in the list. Select the channel and complete the integration.

Note: If it still doesn't work, connect the Slack integration with a **public channel**, then **remove the integration** from the Chatwoot side and reconnect it again.
