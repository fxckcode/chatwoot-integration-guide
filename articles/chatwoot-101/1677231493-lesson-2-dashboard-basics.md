# Lesson 2: Dashboard Basics

In Lesson 1 you sent your first reply. That's enough to support one customer. To support *fifty* without losing your mind, you need to know your way around the dashboard. This lesson is the map.

## What you'll learn

* The four regions of the Chatwoot dashboard and what each one is for

* How to find any conversation fast — by status, assignee, inbox, label, or text

* The four conversation statuses and when to use each

* The difference between Mine, Unassigned, All, Mentions, and Unattended views

* How to set your availability and manage notifications

* The keyboard shortcuts that pay for themselves on day one

**You'll need:** Your inbox from Lesson 1 and at least one test conversation in it. (Send yourself two or three messages from the widget so the dashboard isn't empty.)

---

## The four regions of the dashboard

Almost every screen in Chatwoot is laid out the same way. Once this clicks, the rest of the product becomes obvious.![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTVFJSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b6df0eb6da5419d16b18ea6ac9d97af16495896b/dashboard.webp)

### 1. Navigation rail (far left)

Vertical strip of icons. Top to bottom: **Inbox**, **Conversations**, **Captain** (if AI is enabled), **Contacts**, **Reports**, **Campaigns**, **Help Center**, and **Settings**. This is how you switch *pages* — everything else changes based on where you are here.

### 2. Conversation list (middle-left)

A scrollable list of conversations with filters and tabs at the top. This is where you live during a shift.

### 3. Conversation view (center)

The actual messages plus the reply box. Tabs at the top let you switch between **Reply**, **Private Note**, and (where supported) **Email** mode for outbound messages.

### 4. Context panel (right)

Everything you might need to know about the customer — contact details, previous conversations, custom attributes, conversation actions (assign, label, team, status), and any dashboard apps you've added.

**Tip:** You can collapse the right panel. Useful on small screens or when you're focused purely on the message thread.

---

## The conversation list, in detail

This is the panel you'll spend the most time scanning. Three things to learn:

### Tabs at the top: who owns what

| Tab            | Shows                                           |
| -------------- | ----------------------------------------------- |
| **Mine**       | Conversations assigned to you                   |
| **Unassigned** | Conversations no agent has picked up yet        |
| **All**        | Every conversation in the inbox(es) you can see |

Most teams build their day around **Mine** (work the queue you own) and **Unassigned** (grab the next one when Mine is empty).

### Status filter: where in the lifecycle

Right under the tabs, switch between:

* **Open** — the customer is waiting on a reply

* **Pending** — bot or AI is handling it, not yet ready for a human

* **Snoozed** — set aside until a date/time or until the customer replies

* **Resolved** — done

### Two more views you should know about

* **Mentions** — conversations where a teammate `@`-mentioned you in a private note. Treat this like email — check it daily.

* **Unattended** — assigned conversations that *still* haven't gotten a first reply. This is where managers find dropped balls.

Both live in the navigation as separate views, not under the **Mine/Unassigned/All** tabs.

---

## Filters, folders, and search

### Quick filters (left sidebar)

Below the **Conversations** entry in the nav, you'll find a tree:

* **Inboxes** — filter by a specific channel (just Email, just Website, etc.)

* **Labels** — filter by a label you've applied (`bug-report`, `vip`, etc.)

* **Teams** — filter by the team handling the conversation

* **Folders** — filters *you've saved*

### Folders

Anytime you build a useful filter, click **Save filter as folder** and give it a name. It appears under **Folders** for one-click access. Examples worth saving on day one:

* *VIP customers waiting* — label `vip` + status `Open`

* *Stuck in pending* — status `Pending` + last activity > 1 day

* *My snoozed* — assignee `Me` + status `Snoozed`

### Search

The search bar at the top of the dashboard searches across conversations, messages, contacts, and articles.

---

## Conversation statuses, and when to use which

You'll set conversation status many times a day. Pick the right one and your queue stays honest.

| Status       | Use it when…                                                                | What it does                                                        |
| ------------ | --------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| **Open**     | The customer is actively waiting                                            | Default state — visible in everyone's queue                         |
| **Pending**  | Captain or a bot is handling, and the conversation isn't ready for an agent | Hides from agent default views                                      |
| **Snoozed**  | You're waiting on the customer or internal team                             | Auto-reopens on customer reply or timer                             |
| **Resolved** | The issue is handled                                                        | Drops out of Open; can reopen automatically if the customer replies |

**Rule of thumb:** if you wouldn't want to see this conversation again *today*, snooze it. The Open queue is for things that need attention now.

---

## Your status: Online, Busy, Offline

Bottom left of the dashboard, click your avatar to set:

* **Online** — you're available; auto-assignment sends you new work

* **Busy** — you're around but heads-down; the system avoids assigning new conversations to you

* **Offline** — you're done for the day; new work goes to others

Your status is also visible to teammates, so they know when to ping you.

***Auto-offline:** Chatwoot will mark you offline automatically if you close the tab or go idle, so you won't accidentally hold conversations after logging off*.

---

## My Inbox

My inbox in the navigation shows in-app notifications: new assignments, mentions, conversation creations, and SLA alerts. Click any item to jump straight to the conversation.

## Notifications

You also have four notification *channels* you can configure from **Profile Settings → Notifications**:

* **Audio** — alert sound on the dashboard

* **Email** — for things you'd want to see from your inbox

* **Push** — browser push, even when the dashboard isn't open

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSDhKSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--ab81059792732e067a948b519736f32a22a9d2d8/Screenshot%202026-04-27%20at%201.06.29%E2%80%AFPM.png)

A common starting point: enable **Push** for *Conversation assigned to me* and *Mention*, leave audio on, skip the rest until they prove useful.

---

## Mini-exercise (3 minutes)

Try these in order. They cement everything above:

1. Send yourself two new test messages from the widget so the queue isn't empty.

2. From the dashboard, open the second one and **assign it to yourself**.

3. Apply a label called `practice`.

4. **Snooze** it until tomorrow morning.

5. Click into **Mine**, then **Snoozed** — your conversation should be there.

6. Build a filter: status = Open, label = `practice`. **Save it as a folder** called *Practice queue*.

If everything in that list felt natural, you're ready to actually run a shift.

---

## Common questions

**Why don't I see all my team's conversations?**

You only see inboxes you've been added to. If a conversation is missing, you may not be a member of that inbox — ask an admin.

**My queue feels overwhelming. What do I work first?**

Default order: **Mentions** → **Unattended** → **Mine (Open)** → **Unassigned**. Mentions and unattended are signals that something is off; Mine is your committed work; Unassigned is "new fuel" once the first three are clear.

**A conversation I resolved came back. Did I do something wrong?**

No — that's by design. If a customer replies after you resolve, Chatwoot reopens the conversation automatically so it doesn't get lost.

---

Feeling confident about the dashboard? That probably took 5 minutes! Let us understand all the core features next. [Go to Lesson 3A now](https://www.chatwoot.com/hc/chatwoot-user-guide-cloud-version/articles/1677235281-lesson-3-a-mastering-core-features).
