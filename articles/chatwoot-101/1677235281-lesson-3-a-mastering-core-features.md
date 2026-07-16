# Lesson 3 (a): Mastering core features

You can now find conversations and reply to them. This lesson is about the tools that turn ten minutes of typing into a thirty-second action — the features that good agents use *every single conversation* without thinking about it.

We'll focus on the in-conversation toolkit: private notes, canned responses, labels, macros, conversation actions, and participants. Lesson 3(b) will cover the data-and-context side: contacts, custom attributes, bulk actions, and advanced filtering.

## What you'll learn

* How to talk to your team *inside* a conversation without the customer seeing it

* How to reply in two keystrokes using canned responses

* How to keep your queue organized with labels (and what to actually label)

* How to chain three or four routine steps into a single click using macros

* How to assign, route, snooze, and prioritize from the conversation actions panel

* How to pull teammates into a conversation as participants without handing it off

**You'll need:** A test conversation in your inbox (carry over the one from Lesson 2) and admin access to set up at least one canned response and one macro.

---

## 1. Private Notes — your team's sidebar

A **private note** is a message inside a conversation that *only your team* can see. The customer never sees it, never gets notified, and it never leaves Chatwoot.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQTVNSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--8c1b33a4c7fe687f50238cf7a78dc154d4399b64/private-notes.gif)

Use it for:

* "Looping you in — this looks like a billing edge case."

* "FYI, I already refunded their last order. Don't double up."

* "Customer is a VIP, please prioritize."

### How to send one

1. Open a conversation.

2. Switch the reply tab from **Reply** to **Private Note** (top of the message composer).

3. Type your note. The composer turns yellow so you don't mix them up with public replies.

4. Hit **Send**.

### @mentions inside notes

Type `@` and start typing a teammate/team's name. Selecting them does two things:

* They get a **notification** (in-app, push, and optionally email).

* The conversation shows up in their **Mentions** view.

***Rule of thumb:** if you'd otherwise Slack a teammate about the conversation, write a private note instead. The context stays attached to the conversation.*

---

## 2. Canned Responses — your reply shortcuts

A **canned response** is a saved reply template you trigger with a short code. Instead of retyping "Thanks for reaching out! Could you share your account email so I can look this up?" thirty times a day, you save it once as `/email-ask` and trigger it with two characters.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCR1pMSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--d5b3bcb339902ed88ff215cea5d197198d34d4e4/canned-responses.gif)

### Setting one up

1. Go to **Settings → Canned Responses → Add Canned Response**.

2. Fill in:

   * **Short Code** — what you'll type to trigger it (e.g. `email-ask`)

   * **Content** — the template body. Markdown works.

3. Save.

### Using one in a conversation

In the reply box, type `/` followed by the short code (`/email-ask`). A picker pops up — hit Enter and the full template fills in. Edit if needed, then send.

### What to make canned responses for (start with these five)

* A friendly greeting / opener

* Asking for an account email or order number

* "We're looking into this and will get back to you within X hours"

* A closing line you use to wrap conversations

* A link to your most-shared docs article (refund policy, pricing, install guide — whatever your top hit is)

> **Tip:** Canned responses are *templates*, not robots. Personalize the first sentence — using the customer's name and one detail from their message — before you send.

---

## 3. Labels — the digital sticky notes

A **label** is a tag you attach to a conversation. Labels are account-wide and reusable. Used well, they're how you find patterns ("we got 12 `billing-bug` reports this week") and how you build saved folders ("show me all open `vip` conversations").

### Adding a label to a conversation

* From the **conversation actions panel** on the right: click **Add Label** and pick or create one.

* Or use the keyboard: hit `Cmd+K` to find the shortcut for label-add.

### How to think about labels

Labels work best when you keep the list short, opinionated, and consistent. Three categories cover most teams:

| Category            | Example labels                                           | Why                              |
| ------------------- | -------------------------------------------------------- | -------------------------------- |
| **Topic**           | `billing`, `bug-report`, `feature-request`, `onboarding` | What the conversation is *about* |
| **Customer signal** | `vip`, `at-risk`, `enterprise`                           | Who you're talking to            |
| **Workflow**        | `needs-engineering`, `needs-followup`, `escalated`       | What needs to happen next        |

\
***Anti-pattern:** ten labels that mean almost the same thing (`bug`, `bugs`, `bug-report`, `defect`, `issue`). Pick one and delete the rest. Run a label cleanup once a quarter.*

---

## 4. Macros — chained actions in one click

A **macro** is a saved sequence of actions. Where a canned response is just text, a macro can do *several things at once*: send a reply, add a label, assign a team, snooze the conversation — all in a single click.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQ0ZPSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--99b80ed019cfa19f318d450a5889ca1c60c29f5b/macros.jpg)

### A real example: the "refund issued" macro

When you process a refund, you probably do all of these:

1. Send a templated message confirming the refund

2. Add a `refund-issued` label

3. Assign to the **Finance** team for record-keeping

4. Resolve the conversation

A macro bundles those four steps into a single button.

### Setting one up

1. Go to **Settings → Macros → Add a new Macro**.

2. Name it (e.g. *Refund issued*).

3. Add **actions** in order — the action picker has options like *Send Message*, *Assign Team*, *Add Label*, *Resolve Conversation*, *Send Email Transcript*.

4. Set **visibility**: *Private* (just you) or *Public* (whole team). Save.

### Running a macro

Open any conversation, scroll the right sidebar to **Macros**, pick yours, and click **Run**. Done.

***When to write a macro:** any time you find yourself doing the same three or four actions back-to-back more than a few times a week. Five minutes setting up the macro saves you hours over a quarter.*

---

## 5. Conversation Actions — the right sidebar in detail

The **conversation actions** panel (right side, top section) is where you change the state of a conversation. Quick tour:

| Action                  | Use it for                                                                    |
| ----------------------- | ----------------------------------------------------------------------------- |
| **Assignee**            | Hand the conversation to a specific agent                                     |
| **Team**                | Route to a group (Engineering, Billing, CS) so any team member can pick it up |
| **Conversation Status** | Open / Pending / Resolved / Snoozed (covered in Lesson 2)                     |
| **Priority**            | Low / Medium / High / Urgent — shows up in queue sorting and SLA calculations |
| **Add Label**           | Apply one or more labels                                                      |

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSDlPSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--db48e5b9b916261d6df3f31cffd5bc244a8b6a62/conversation-actions.jpg)

***Status vs assignee:** changing **assignee** moves who's responsible; changing **status** moves where it sits in the workflow. They're independent — you can have a Resolved conversation with an assignee, or an Open conversation that's unassigned.*

---

## 6. Conversation Participants — collaborate without handing off

Sometimes you need a teammate's eyes on a conversation, but you don't want to *give it to them*. That's what **participants** are for.

* **Assignee** = the one person responsible for replying.

* **Participant** = anyone else who's watching and can chime in.

* 

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCT1JPSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--46758000b4b5c586b9c95425039c5381f2a89276/conversation-participants.jpg)

### How to add one

In the conversation actions panel, click **Participants → Add** and pick teammates. They'll get notifications for new activity on the conversation, and it'll show up in their **Participating** view.

### When to use it

* A senior agent shadowing a junior agent's reply

* Pulling in an engineer for a technical thread without making them own customer comms

* Keeping a manager in the loop on an escalated case

> **Don't** add the whole team as participants — that's notification spam. Two or three people max, with a reason.

---

## Mini-exercise (5 minutes)

1. Create one canned response. Use shortcode `hi` and content *"Hi {{*[*contact.name*](http://contact.name)*}}, thanks for reaching out — how can I help?"*. (The `{{contact.name}}` placeholder auto-fills the customer's name.)

2. Create one macro called *Wrap up* that adds a `resolved-by-me` label and resolves the conversation.

3. Open your test conversation. Send a private note `@teammate trying out mentions`.

4. Trigger your `/hi` canned response.

5. Run the *Wrap up* macro.

If all five worked, you've used the entire core toolkit.

---

## Common questions

**Can the customer ever see private notes or macro internals?**

No. Private notes and macro action steps (assign, label, etc.) are invisible to the customer. Only macro actions of type *Send Message* go to the customer — and those look like normal replies.

**Can I edit a canned response after the fact?**

Yes. **Settings → Canned Responses**, click any row, edit, save. Existing usages (already-sent messages) aren't changed retroactively.

**What's the difference between assigning a team vs. an agent?**

Assigning to an **agent** says "this is yours specifically." Assigning to a **team** says "anyone on this team can pick it up." Most teams use team assignment for routing and agent assignment for ownership.

**Should I label every conversation?**

You don't have to label every conversation, but a quick label on closing — even just one — pays off enormously when you look at reports later. Make it a habit on resolve.

**Macros don't run automatically?**

Correct — macros are *manual*. If you want something to run automatically based on a trigger (like "auto-label any conversation containing the word 'refund'"), that's an **Automation Rule**, which we'll cover in a later lesson.

---

## What's next

In **Lesson 3(b): Working with customer context**, we'll switch focus from *what you do to a conversation* to *what you know about the customer*: the contact record, custom attributes, previous conversations, bulk actions across many conversations at once, and saved filters that turn a chaotic queue into a focused workspace.
