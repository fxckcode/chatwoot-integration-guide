# Service Level Agreements

As the service provider, your Service Level Agreements (SLAs) are contractual arrangements between you and your customers that define the level of service you commit to deliver. Your SLAs specify the expected performance metrics, such as response times, availability, and resolution times, that you have agreed to provide. These SLAs hold you, as the service provider, accountable for the quality of service you deliver, ensuring a consistent and reliable level of support for your customers.

Chatwoot allows you to track the following metrics:

* FRT (First Response Time): This metric refers to the time it takes for the agent to respond to a customer's initial inquiry or request. It is a critical measure of responsiveness, as customers expect prompt attention to their issues or questions.

* NRT (Next Response Time): This metric focuses on the time between the customer's follow-up message and the agent's subsequent response. It ensures that the provider maintains a consistent level of engagement and keeps the conversation moving forward.

* RT (Resolution Time): This metric captures the total time it takes for the agent to fully resolve the customer's issue or query, from the initial contact to the final resolution. It is a key indicator of the provider's efficiency and effectiveness in addressing customer needs.

## Creating an SLA

You can configure SLAs from the settings page, an admin is allowed to create and delete SLAs, **please note that you cannot modify or change an SLA once it's created.** To create an SLA, you need to add at-least one metric to be tracked.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBd2tibmc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--2f891f1ef9ab8207033f90217321e2db853e9e6a/CleanShot%202024-04-15%20at%2013.44.30@2x.png)

## Applying an SLA

You can use an [automation rule](https://chatwoot.help/hc/user-guide/articles/1677689800-how-to-use-automation) to assign an SLA when a conversation event is triggered. Here's an example of assigning the "Enterprise P0" SLA when a conversation is created by a specific email address and the priority is set to Urgent.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBeFlibmc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--4f46e44c9ccf4ca5d061e3c4fb4d670326afdb72/automation-rule.png)

Once a conversation matches the SLA conditions and the events, the SLA policy is automatically applied. **Once an SLA is applied, it cannot be removed from the conversation.**

Conversations with an active SLA, which is close to a threshold will show up in the UI as follows

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBN1ljbmc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--9700b77a0f29c02c220346a503132b219c0b1cf3/sla-chips.png)

## Applying SLA for a Team  

You can use Automation Rules to automatically apply specific SLAs to conversations handled by different teams.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCREhFcXdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b4709b1dcf03552c2ea075d11f73180ccd007005/SCR-20260624-oeuh.png)

In the example above, the automation rule monitors the assigned team and the conversation status. When a conversation is assigned to the **Sales Team**, the **Enterprise PO SLA** is automatically applied, and SLA tracking begins immediately.

Similarly, you can create automation rules to apply different SLAs based on inboxes, companies, contacts, assignees, custom attributes, and more. By combining Automation Rules with SLAs, you can tailor response and resolution targets to match your unique support and business workflows.
