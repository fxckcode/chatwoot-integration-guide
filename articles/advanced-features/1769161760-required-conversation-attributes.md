# Required Conversation Attributes

Required Conversation Attributes lets admins enforce that agents fill in specific custom attributes before resolving a conversation. This ensures your team captures structured data consistently whether it's a resolution category, severity level, or any other field important for reporting and quality tracking.

## How it works

When an admin configures required attributes, agents will be prompted with a modal whenever they try to resolve a conversation that is missing those values. The conversation cannot be resolved until all required fields are filled.

If the attributes already have values (set earlier during the conversation), the resolution proceeds normally without any prompt.

Setting up required attributes:

1. Navigate to Settings → Conversation Workflows.

2. Under Attributes required on resolution, click Add Attributes.

3. Select one or more conversation-level custom attributes from the dropdown.

4. The selected attributes are now enforced on resolution.

5. To remove an attribute from the required list, click the delete icon next to it.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRDNuaVFNPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--4a701ce7413142ff814e7be3c3abcbadc84ae716/CleanShot%202026-01-23%20at%2013.45.50@2x%201%20(1).png)

## Agent experience

When an agent clicks Resolve on a conversation that is missing required attributes:

1. A modal appears listing all the unfilled required attributes.

2. The agent fills in the values using the appropriate input for each type text, number, link, date, list, or checkbox.

3. Once all fields are completed, the agent clicks Resolve conversation to save the values and resolve in one step.

If the agent is not ready to resolve, they can click Cancel to return to the conversation without making changes.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTC9waVFNPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--bce3a84d0f022ab01f8e10e90b6a25c9e387c0ea/copilot-2.png)

## Supported attribute types

You can mark any conversation-level custom attribute as required. The supported types are:

* Text - Free form text input

* Number - Numeric value

* Link - URL (validated for correct format)

* Date - Date picker

* List - Dropdown selection from predefined options

* Checkbox - Yes/No selection

## Bulk actions

When bulk-resolving conversations, the same rules apply. Conversations that are missing required attributes will be skipped, and a notification will inform the agent that those

conversations could not be resolved. The remaining conversations that satisfy the requirements will be resolved normally.

## Things to note

* Only admins can configure which attributes are required.

* Required attributes are enforced only on manual resolution (individual or bulk). API-based resolution does not enforce the attribute check.

* If a custom attribute definition is deleted, it is automatically removed from the required list.

## Availability

Review Notes are available on:

* **Cloud**: Business and Enterprise plans

* **Self-hosted**: Available in all self-hosted paid plans
