# Lesson 3 (b): Working with Customer Context

Lesson 3(a) was about what you do *inside* a conversation. This lesson is about what you know about the *person* on the other end and how to use that knowledge to give better, faster, more personal support.

The shift in mindset: stop thinking of each conversation as an isolated message thread. Start thinking of it as the latest entry in a long relationship with a specific human being, one who has a name, a history, an account, and a set of facts you should know before you reply.

## What you'll learn

* How to read a contact record at a glance

* How to use a customer's previous conversations to answer faster

* What custom attributes are and how they make replies smarter

* How to take action on dozens of conversations at once with bulk actions

* How to turn complex filters into one-click saved folders and segments

* How to find anything — fast — using global search

**You'll need:** A few test conversations from the same contact (send 2-3 messages from the widget so you have history to play with).

---

## 1. The contact record — your customer's profile

Every person who messages you becomes a **contact**. The contact record is the one place where everything you know about that person lives.

### What the contact record contains

| Section               | What's in it                                                                  |
| --------------------- | ----------------------------------------------------------------------------- |
| **Identity**          | Name, email, phone, profile photo, locale                                     |
| **Company**           | Organization the contact belongs to (for B2B teams)                           |
| **Conversations**     | Every conversation they've ever had with you, across all channels             |
| **Custom Attributes** | Any custom data you track about this contact                                  |
| **Notes**             | Free-form notes about the customer (separate from conversation private notes) |

### Two minutes that change every reply

Before you reply to anything non-trivial, glance at three things in the contact panel:

1. **Their name** — use it in the reply.

2. **Previous conversations** — if they wrote in last week, you should know what about.

3. **Custom attributes** — plan, signup date, account ID. The "boring" facts are usually the ones that change your answer.

***Tip:** "I see you wrote in last Tuesday about the same export bug — let me check on the fix" is the difference between a generic support reply and one that feels like you actually care.*

---

## 2. Previous conversations — the history that already exists

Inside any conversation, the right sidebar has a **Previous Conversations** section. It lists every prior thread with this contact, regardless of channel.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSTFQSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--c5619d75a0e5765f0372f8bad85d9c1cd99208ef/previous-conversations.jpg)

### Why this matters

Customers don't think in conversation IDs. They think *"I told you about this last month."* If you can pull up that thread in one click, you save them the frustration of re-explaining and you save yourself the trouble of asking.

### How to use it well

* **Skim, don't read.** Look at the resolved threads' subject lines and labels. You're looking for *patterns* (this customer always asks about exports) more than specifics. Use Captain to summarize previous thread to make it easier.

* **Look at recent labels.** If the last three conversations are labeled `billing`, today's "quick question" probably isn't.

* **Open the most recent one in a new tab** if you need full context — keep your current conversation open in the original tab.

---

## 3. Custom Attributes — the data your replies depend on

A **custom attribute** is a field *you* define on contacts or conversations to track something specific to your business.

Standard contact fields (name, email, phone) are universal. Custom attributes are the things only your business cares about: subscription plan, signup date, MRR, last login, account ID, customer tier.

### Two flavors

* **Contact custom attributes** — facts about the *person* (e.g. *Plan*, *Signup Date*, *Lifetime Value*).

* **Conversation custom attributes** — facts about the *conversation* (e.g. *Order Number*, *Bug Severity*, *Refund Amount*).

### Setting one up

1. Go to **Settings → Custom Attributes → Add Custom Attribute**.

2. Choose **Applies To**: *Contact* or *Conversation*.

3. Pick a **type**: Text, Number, Link, Date, List (dropdown), or Checkbox.

4. Name it and add a description. Save.

The new attribute now appears in the right sidebar of every contact or conversation, ready to be filled in.

### How custom attributes make you faster

* They populate **canned response variables** — `{{contact.custom_attribute.plan}}` in a template auto-fills the customer's plan.

* They power **filters** — "show me all open conversations from `Enterprise` plan customers."

* They drive **automation rules** — "auto-assign Enterprise customers to the senior team."

***Where the data comes from:** for SaaS, you'll usually populate custom attributes via the *[*identify API*](https://www.chatwoot.com/developers/api/) when a logged-in user opens the chat widget. Attributes you fill in by hand also stick.

---

## 4. Bulk Actions — handling many conversations at once

Some days the queue is fine. Other days you come back from lunch to forty new conversations from the same outage. **Bulk actions** are how you process them at scale.

### How to trigger bulk mode

In the conversation list, hover over a conversation and a **checkbox** appears on the left. Tick one and a selection bar shows up at the top. Tick more, or hit **Select all**, to act on the whole batch.

### What you can do in bulk

* **Assign agent or team**

* **Add or remove labels**

* **Change status** (resolve, snooze, reopen)

---

## 5. Saved filters — folders and contact segments

You met **Folders** briefly in Lesson 2. Now we'll go deeper, and meet their cousin: **Contact Segments**.

### Folders (for conversations)

A folder is a saved conversation filter. It always reflects current data, open the folder and you see the latest matches, not a frozen snapshot.

**Build one:**

1. Click **Conversations → Custom view → New filter**.

2. Add conditions: status, assignee, inbox, labels, custom attributes, dates, etc. Combine them with `AND` / `OR`.

3. Click **Save filter** and give it a name.

It now lives under **Custom Folders** in the left rail, one click away.

### Contact Segments

A **contact segment** is the same idea, applied to your contacts directory. *"All contacts on the Enterprise plan who have written in this month"* becomes a one-click view you can revisit any time.

**Build one:**

1. Go to **Contacts → All Contacts → Filter**.

2. Add conditions on standard fields and custom attributes.

3. Click **Save filter as segment**.

***Folders compound.** The folders you save in week one will still be saving you time in year two. Build them as you go.*

---

## 6. Global search

Click on search input on the navigation from anywhere in the dashboard to focus the global search bar. It searches across:

* **Conversations** — by message text, subject, or ID

* **Contacts** — by name, email, phone, identifier

* **Articles** — your Help Center content

### When to use search vs. filters

* **Search** when you remember a specific phrase, name, or number. *"Did Sarah mention the export bug?"*

* **Filters/folders** when you want to see a *category* of conversations. *"All open billing tickets."*

If you're typing the same search query more than twice a week, that's a filter waiting to be saved as a folder.

---

## Mini-exercise (6 minutes)

1. Create a contact custom attribute called `Plan` (List type, options: `Free`, `Pro`, `Enterprise`).

2. On your test contact, set `Plan` = `Pro`.

3. Update your `/hi` canned response from Lesson 3(a) to include `{{contact.custom_attribute.plan}}` somewhere — e.g. *"Hi {{*[*contact.name*](http://contact.name)*}}, thanks for reaching out about your {{contact.custom_attribute.plan}} plan."*

4. Trigger `/hi` in a conversation. The plan should auto-fill.

5. Build a filter: *Status = Open AND Plan = Pro*. Save it as a folder named *Pro queue*.

6. Send yourself two more test messages, tick their checkboxes in the queue, and bulk-apply a label `practice`.

If all six worked, you've graduated from "I can use Chatwoot" to "I can run a shift in Chatwoot."

---

## Common questions

**A contact has duplicate entries — same person, two records. Why?**

Usually they wrote in from two different channels (e.g. email and website chat) before the system could match them. Open one record and use **Merge contact** to combine them. Conversation history from both is preserved.

**Can I edit standard contact fields?**

Yes. Click any field in the contact panel and edit inline. Changes save immediately.

**Can i use custom attributes in filters?**

Yes, they appear as filter options for both conversations and contacts. They're also exposed in canned response variables.

**Are bulk actions in conversations reversible?**

The action itself cannot be reversed, but the outcome is reversible. You can re-assign, remove a label that was added etc, but the history of the previous action remains in the activity messages.

**Why do I see different contacts in different inboxes?**

You don't. Contacts are account-wide. But conversations are scoped to inboxes. If you can see only some inboxes, you'll see only some of that contact's conversations. Ask an admin if you think you're missing inbox access.

---

## What's next

You've now mastered the core agent toolkit, from layout (Lesson 2) to in-conversation tools (3a) to customer context (3b). In **Lesson 4**, we'll zoom out from individual conversations to the systems that handle volume: **automations**, **SLAs**, **business hours**, and the routing rules that make sure the right conversation reaches the right agent before *you* even have to think about it.
