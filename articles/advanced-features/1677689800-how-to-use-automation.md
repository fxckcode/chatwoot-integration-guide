# How to use Automation?

Chatwoot's automation feature streamlines team workflow by automating repetitive tasks and saving time. It allows for various actions such as assigning labels, and teams and routing conversations to the most suitable agent, enabling the team to focus on their core responsibilities and spend less time on manual tasks.

## How does Automation work?

An automation rule is made up of three things––An **Event**, **Conditions**, and **Actions**. The Event is the trigger for automation to perform itself. The conditions are criteria that must be met before the actions are executed. The Actions are tasks that will be executed when the conditions are met.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBOWQ0VHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--945e25fe97afe0d8c1c00514d0daf811021dbe62/chatwoot%20automation%20workflow.png)

### Automation Events

Automation Events are triggers that initiate the execution of automation. Chatwoot currently offers three types of events.

1. **Conversation created:** A trigger/event initiated when a new conversation is created. This includes conversations created in all channels.

2. **Conversation updated:** A trigger/event initiated when a conversation is updated.

3. **Message created:** A trigger/event initiated when a new message in a conversation is created.

4. **Conversation opened:** A trigger/event initiated when a previously snoozed, resolved, or pending conversation is opened again.

### Automation Conditions

Conditions are the criteria that must be met before the actions are performed. They are evaluated in the order they are defined.

Conditions depend on the type of event you select. Here is a comprehensive list:

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBL2w0VHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--1c41c3fe7ca08e51859af0379013a7c87cf5a871/automation%20events%20and%20available%20conditions.png)

### Automation Actions

Actions are tasks/processes that are executed whenever respective conditions are met. Chatwoot currently supports the following actions:

* Assign to agent

* Assign a team

* Add a label

* Send an email to team

* Send an email transcript

* Mute conversation

* Snooze conversation

* Resolve conversation

* Send Webhook Event

* Cancel

* Send Attachment

* Send a message

These actions are available irrespective of the Events or Conditions you choose.

## How to create an Automation rule?

**Step 1.** Go to Settings → Automation. Click on the “Add Automation Rule” button.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBL3g0VHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--da41e558aa88f2531bc9025b3bc955045b508390/adding%20automation%20rule%20in%20chatwoot.png)

**Step 2.** An automation rule creation modal will open up. Start filling the fields as listed below.

1. Give your automation a name to easily refer to it later.

2. Add a description (optional).

3. Select an event from the dropdown menu.

4. Add conditions. Use `equal to` or `not equal to` operators to define the conditions.

5. Add actions.

You can add multiple conditions and actions as well. Use `AND`, `OR` operators to do this.

**Example**

You want to assign all new conversations to the France sales team whenever the Browser language is French. Here’s how you can create an automation rule for this –

1. Add a name and a description.

2. Select event as `Conversation Created`.

3. Add two conditions and join them with the `AND` operator. Condition 1: `Conversation Status` is `Open`, and Condition 2: `Browser Language` is `Francais (fr)` from the dropdown.

4. Add an action - `Assign a team` and select the team `France sales` from the dropdown. (You need to create your team first).

   ![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBLzU0VHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--82ba76a00077245693892b2a8e830740d1dbeb47/automation%20settings%20in%20chatwoot.png)

   ## How to pause, edit, clone, and delete automation rules?

   Your list of Automation rules appears under “Automations”. You can view this page by going to **Settings → Automation.** You will find a set of quick actions here:

   ![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBLzk0VHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--2034e74164152283256f5911e2a99ed46d1da117/editing%20automation%20in%20chatwoot.png)

   **To pause an automation rule:**

   Toggle the switch off under the “Active” column.

   **To edit a rule:**

   Click on the pencil icon.

   **To clone a rule:**

   Click on the copy icon.

   **To delete a rule:**

   Click on the red cross icon.
