# How to use Agent bots?

AgentBot lets you connect external AI agents and custom bot logic directly to your Chatwoot inbox. It allows your bot to listen to customer conversations, process incoming queries, and respond through Chatwoot in real time.

Once an AgentBot is connected to an inbox, new conversations are automatically assigned a *pending* status. Chatwoot then sends conversation events to your configured bot URL as webhook events. Your AgentBot can process these events, generate the right response using your own logic or AI systems, and send messages back to the conversation using Chatwoot APIs.

This makes it easy to bring your own AI agent, automation workflow, or external customer support bot into Chatwoot while still keeping human handoff available when needed. 

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBODA0VHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--94aa6ada15f0ff95078e720fa52800b6c087def3/agentbot-logic-chatwoot.png)

## How does the AgentBot work?

Explained below in a typical workflow of an AgentBot.

1. The AgentBot receives events such as `widget_triggered`, `message_created`, and `message_updated` based on customer interactions.

2. The AgentBot processes the received information to generate an appropriate response.

3. The AgentBot can also utilize external system APIs to gather additional customer information, such as order status or booking triggers.

4. The AgentBot can integrate AI models like OpenAI, Claude, Gemini or tools like Amazon Lex to understand what the customer wants.

5. The AgentBot can post the generated response back into the widget by utilizing Chatwoot APIs such as [Create New Message](https://developers.chatwoot.com/api-reference/messages/create-new-message).

6. The AgentBot can toggle a conversation status to open to hand off the conversation to a human agent.

7. It continues to monitor open conversations to provide contextual information to the support agent.

## How does the Human-Agent handoff work?

When an agent bot is connected to an inbox, conversations are created with a "pending" status, allowing it to triage the conversation before passing it on to a human agent.  \
 \
If the bot determines that a human agent's assistance is needed or if the customer explicitly asked for human help, it can use the conversation update API to change the status to "open" which would make the conversation available to a human.

Sometimes the agents would want to push back a conversation which was handed off, back again into the bot queue. Agents can return a handed-off conversation to the bot queue by changing the status back to "pending”.

## How can I use the AgentBot?

Listed below are a few examples.

1. Businesses with high volume customer support queries can utilize an AgentBot to authenticate and filter queries, reducing the workload on human agents and improving the efficiency of customer support.

2. E-commerce websites can integrate the AgentBot with their existing databases, providing customers with real-time updates on order and shipping status, as well as answering other related queries.

3. News and content websites can use the AgentBot to send recommendations to users via card messages.

4. Hotel and movie booking websites can use the AgentBot to handle bookings, reservations and answering related queries, providing customers with a seamless and convenient booking experience.

### Examples

1. [Hotel booking implementation using Dialogflow](https://github.com/chatwoot/dialogflow-agent-bot-demo).

2. [Example implementation using Rasa](https://github.com/chatwoot/rasa-agent-bot-demo).

Also, look into interesting ways to [leverage bot-message types on Chatwoot](https://www.chatwoot.com/docs/product/others/interactive-messages).

## Creating agent bots

### How to create agent bots in your Chatwoot account?

You can create agent bots from the account settings. Go to Settings -> Bots. You will see an option like the one below.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCUE9xVmdFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--7bdf72ebbdc4c17c195f71137b30ce5f5bad5147/Screenshot%202025-05-02%20at%2010.17.45%E2%80%AFAM.png)

Click on "Add Bot" to create a new bot. You will see an option to provide a name, avatar and a webhook URL.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQ09yVmdFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--336219625caefda41e56afd13e204a72304db075/Screenshot%202025-05-02%20at%2010.18.32%E2%80%AFAM.png)

### How to connect an inbox to a bot?

Open the inbox where you want to link the bot. In **Bot Configuration**, pick the bot that should manage the conversations. After you click **Save**, you’ll start getting webhook events each time a new conversation or message is created.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSENyVmdFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--03b4d2a0fc6216c094e8374571d4b3b7b110b64a/Screenshot%202025-05-02%20at%2010.19.58%E2%80%AFAM.png)

For more details about the events that are supported in the webhooks, please visit the Webhook documentation [here](https://www.chatwoot.com/hc/user-guide/articles/1677693021-how-to-use-webhooks).

### Webhook Verification

Once you create an agent bot, we automatically generate a secret that you can use to verify the payload your application receives. You can read more about webhook verification [here](https://www.chatwoot.com/hc/user-guide/articles/1677693021-how-to-use-webhooks#verifying-webhooks).
