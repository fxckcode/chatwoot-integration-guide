# How to bring your Dialogflow chatbot to Chatwoot?

Chatbots are valuable for many customer engagement teams. They efficiently handle trivial questions and free human agents to focus on more pressing issues.

Dialogflow and [Rasa.ai](http://Rasa.ai) are leading NLP (Natural Language Processing) platforms for building customized chatbots. In this guide, we explain how you can create a bot in Dialogflow and easily integrate it with Chatwoot in seconds.

## How to create a Dialogflow bot?

**Step 1.** Go to your [Dialogflow Console](https://dialogflow.cloud.google.com/). We will be using Dialogflow Essentials for this article. Click on "Create Agent". You will see options like these:

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBeENJVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--6d9926ae1dc31a8250ec6fc01dcff523501c80c6/create%20agent%20in%20dialogflow%20console.png)\
**Step 2.** You will need to create intents based on how you want your bot to respond. There will be 2 default intents in the project called "Default Fallback Intent" and "Default Welcome Intent", as shown below.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBeEdJVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--84b949a70c890b4d912e7e0675f35c974a40bd12/creating%20intents%20in%20dialogflow.png)

This completes the basic bot configuration. Let us create a service account and connect it with Chatwoot.

> You can also create additional intents for your specific use cases.\
> Chatwoot also supports advanced intents that enables [agent handoff](https://www.chatwoot.com/docs/product/channels/live-chat/integrations/dialogflow/#creating-a-handoff-intent), [interactive messages](https://app.chatwoot.com/hc/chatwoot-user-guide-cloud-version/en/advanced-features-explained/495), etc.\
> refer: Scroll down to "Advanced Intents".

**Step 3.** Create a service account[​](https://www.chatwoot.com/docs/product/channels/live-chat/integrations/dialogflow/#create-a-service-account "Direct link to heading"). To connect this bot with Chatwoot, you need to create a service account on your Google Cloud console. Navigate to the project console in Google cloud by clicking on the **Project ID** in the project settings.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBMUtJVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--0609885eaed20b42c79ac5b88d09602449d97a2f/project%20ID.png)

Navigate to **IAM & Admin -> Service Accounts**. You will see a view like the one shown below. Click on "Create Service Account".

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBMU9JVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--6678ad3e6c5c9536cfd2dd5d1b83766b459486d6/service%20accounts.png)

Provide a Service Account name and description as shown below.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBMVdJVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--444a6e86cf22a04c36bc4a0de153cf836fe17600/setting%20service%20account%20up.png)

To provide access, select Dialogflow API Client from the dropdown.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBMWFJVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--f0814a4a0a8f6d84a0aa3dfd96c566cd46c18014/dialogflow%20api%20client.png)

Continue and click on "Done". Now, you would be able to see the service listed in the dashboard. The next step is to create a key so that it can be shared with Chatwoot. Click on the service account and click on the "Keys" tab. Then, click on "Add Key". You will be able to see a screen like the one below.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBMktJVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b67cdd18d8a10c64e3ba983808fb15f65543644e/api%20key.png)\
Click on "JSON" and click on "Create". It will generate a key for your service account. Download the key and save it for use later.

## Setting up Dialogflow Integration in Chatwoot[​](https://www.chatwoot.com/docs/product/channels/live-chat/integrations/dialogflow/#configuring-dialogflow-integration-in-chatwoot "Direct link to heading")

Chatwoot has a native Dialogflow integration. You can connect your bot with Chatwoot in two quick steps.

**Step 1.** Go to "Settings -> Applications -> Dialogflow". Click on "Configure".

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBeDJKVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--e3852efe92d0c5e6c0c04751a0942db20dad9608/adding%20dialogflow%20option%20in%20chatwoot.png)

**Step 2.** Click the "Add a new hook" button. it will open up a setup modal. You need to add "Project ID," "Project Key file," and an inbox to create a hook. Copy the contents of the key file downloaded earlier and paste it into the text area.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBeDZKVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--5d23fddf59970ebc4573e7bfda3bddac0c8113f4/dialoglow%20settings.png)

That's it! The integration is complete. Test out the website inbox to see if the bot handles the initial query.

## Advanced Intents[​](https://www.chatwoot.com/docs/product/channels/live-chat/integrations/dialogflow/#advanced-intents "Direct link to heading")

### Creating a handoff intent[​](https://www.chatwoot.com/docs/product/channels/live-chat/integrations/dialogflow/#creating-a-handoff-intent "Direct link to heading")

Once the user requests to talk to the agent, Dialogflow must inform Chatwoot that an agent can take over the conversation.

Create an intent named "Handoff Intent" with training phrases like "Talk to an agent" or "Speak with an agent," etc. To handle the handoff intent, we will create a "Custom Payload" response, as shown below.

```
{
  "action": "handoff"
}
```

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBM2lKVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--09cb509c898b8226a50c99a3ca288ef24f646438/handoff%20intent.png)

Upon triggering an intent with the above payload, Chatwoot will toggle the status of the conversation to `open` and hand it off to an agent.

### Interactive Messages[​](https://www.chatwoot.com/docs/product/channels/live-chat/integrations/dialogflow/#interactive-messages "Direct link to heading")

**Note**: Interactive messages are supported only in the website inbox currently.

Chatwoot-Dialogflow integration also supports [interactive messages](https://app.chatwoot.com/hc/chatwoot-user-guide-cloud-version/en/advanced-features-explained/495). The following types of interactive messages are supported.

1. [Options](https://app.chatwoot.com/hc/chatwoot-user-guide-cloud-version/en/advanced-features-explained/495) (follow-up supported)

2. [Cards](https://app.chatwoot.com/hc/chatwoot-user-guide-cloud-version/en/advanced-features-explained/495)

3. [Articles](https://app.chatwoot.com/hc/chatwoot-user-guide-cloud-version/en/advanced-features-explained/495)

#### **Creating an interactive message Intent**[**​**](https://www.chatwoot.com/docs/product/channels/live-chat/integrations/dialogflow/#creating-an-interactive-message-intent "Direct link to heading")

You can create other interactive messages by changing the payload as mentioned in the [interactive messages guide](https://www.chatwoot.com/docs/product/others/interactive-messages).

Create an intent with required training phrases and a "Custom Payload" response, as shown below for an options message.

```
## example for an options interactive message
{
  "content_type": "input_select",
  "content": "Select your favorite food from below",
  "content_attributes": {
    "items": [
      {
        "value": "I like sushi",
        "title": "Sushi"
      },
      {
        "title": "Biryani",
        "value": "I like biryani"
      },
      {
        "title": "Pizza",
        "value": "I like pizza"
      }
    ]
  },
  "private": false
}
```

When a user interacts with input messages and selects a value, it returns to Dialogflow. This allows for configuring follow-up intents, such as creating an intent with the training phrase "I like biryani" for cases where the contact selects the "biryani" option.

## How can an agent transfer the conversation back to Dialogflow bot?[​](https://www.chatwoot.com/docs/product/channels/live-chat/integrations/dialogflow/#how-can-an-agent-transfer-the-conversation-back-to-dialoflow-bot "Direct link to heading")

When the Dialogflow bot is connected to an inbox, conversations are created with `pending` status instead of `open`. This lets the initial triaging happen via the bot before the conversation is passed on to an agent. When [`handoff`](https://www.chatwoot.com/docs/product/channels/live-chat/integrations/dialogflow/#creating-a-handoff-intent) happens, the conversation status is changed to `open` and the bot stops responding to it.

Sometimes the agents would want to push back a conversation that was handed off, back again into the bot queue. They can do this by changing the conversation status back to `pending`. This will make the bot start responding to that conversation again.
