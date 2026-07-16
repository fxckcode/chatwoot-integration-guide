# Updating your Account settings

The **Account Settings** page is where an administrator sets top-level details about the Chatwoot account itself — its name, default language etc.

**Where to find it:** **Settings → Account Settings**. The page header reads *"Account settings"*.

**Who can access it:** administrators only. Regular agents and custom roles cannot view or edit this page.

---

## General settings

All fields are saved together using the **Update settings** button at the bottom.

| Field | Required | Description | 
|-------|----------|-------------| 
| **Account name** | Yes | Display name for the account, shown in account switchers and on email transcripts. | 
| **Site language** | Yes | Default UI language for the dashboard. Individual users can override this in Profile Settings. |

\
![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQWVkSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--4b6c27ad77641ca97f62756d3e379c75d738a75f/account-settings.jpg)

---

## Transcribe Audio Messages

When enabled, Chatwoot automatically generates a text transcript whenever an audio message is sent or received in a conversation, and shows it inline alongside the audio.

This section only appears when **Captain** is enabled on your account. Saving is automatic on toggle.

---

## Account ID

A read-only display of your account's unique numeric ID, shown in a copyable code block. You'll need it whenever you build an integration against the Chatwoot Application API. Click the code to copy.

---

## Delete your Account

Only displayed on Chatwoot Cloud installations.

Clicking **Delete Your Account** opens a confirmation modal. To confirm, type the account's exact name into the field and click **Delete**. The account is then **marked for deletion** at a future scheduled date — not removed immediately.

If the account is already marked for deletion, this section instead shows a red banner with the deletion date and a **Cancel Scheduled Deletion** button. Two banner variants exist:

* *"This account is scheduled for deletion on {date}. This was requested by an administrator."* — manual deletion

* *"This account is scheduled for deletion on {date} due to account inactivity."* — inactivity-based deletion

Cancelling reverts the deletion as long as the scheduled date hasn't passed.

---

## Build info

A small footer at the bottom of the page showing:

* The current Chatwoot version (e.g. *v3.16.0*)

* The Git build identifier, clickable to copy the full value

If a newer version is available, an additional line appears above on self-hosted installations: *"An update {version} for Chatwoot is available. Please update your instance."*

Useful for support tickets — paste the version and build identifier when reporting an issue.
