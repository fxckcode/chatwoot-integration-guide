# Lesson 6: Reports and Metrics

You can now run a queue (Lessons 1–3), you've automated the routine work ([Lesson 4](https://www.chatwoot.com/hc/user-guide/articles/1677238266-lesson-4-complete-your-customer-engagement-suite)), and you've put AI to work on your behalf ([Lesson 5](https://www.chatwoot.com/hc/user-guide/articles/1777328078-lesson-5-ai-actions)). This lesson is about the *other half* of running a support operation: knowing what's working.

Reports turn the firehose of conversations into numbers you can act on, how fast you reply, where conversations get stuck, who's handling what, and whether your customers are happy.

## What you'll learn

* 9 reports Chatwoot offers and what question each one answers

* The six core metrics that show up across most reports

* How CSAT scoring actually works

* How to read the live Overview and the conversation heatmaps

* When to turn on the business-hours filter (and when not to)

* How to export any report to CSV for deeper analysis

**You'll need:** A few weeks of conversation data is ideal, reports on an empty account don't tell you much. If you're testing on a fresh install, send yourself a stream of test messages over a few sessions before exploring.

---

## Where reports live

Click **Reports** in the navigation. You'll see tabs along the top for the different report types. Most reports follow the same layout:

* **Time-range picker** at the top (last 7 days, 30 days, 3 months, 6 months, 1 year, or a custom range)

* **Group by** option (day, week, month, year — automatically expands as your range grows)

* **Business hours** toggle (more on this below)

* **Entity filter** specific to the report (which agent, which inbox, which label, etc.)

* The **chart** itself, with a CSV download button on most reports

Once you understand the layout once, every report behaves the same way.

---

## The six core metrics

Five of the reports — Conversation, Agent, Inbox, Team, and Label — show the *same* set of metrics, just sliced differently. Learn these once and the rest is just "the same thing, grouped by agent" or "the same thing, grouped by label."

| Metric                      | What it measures                                                                                                     |
| --------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **Conversations Created**   | Total new conversations in the time window                                                                           |
| **Incoming Messages**       | Messages sent by customers                                                                                           |
| **Outgoing Messages**       | Messages sent by your team                                                                                           |
| **Avg First Response Time** | Average time from a customer's first message to your team's first reply                                              |
| **Avg Resolution Time**     | Average time from a conversation being created to being resolved                                                     |
| **Resolutions Count**       | How many conversations reached *Resolved* status                                                                     |
| **Avg Reply Time**          | Average time between a customer message and the next agent reply (across the whole conversation, not just the first) |

*Avg first response time* and *avg reply time* are different. First response is one number per conversation. Avg reply time is the average across *every* exchange in *every* conversation which is a better measure of ongoing responsiveness, not just opening speed.

---

## The reports, one by one

### 1. Overview (Live)

**Question it answers:** *"What's happening right now?"*

The only real-time report. No date range — it always shows current state.

* **Open / Unattended / Unassigned / Pending counts** for the whole account

* **Agent status distribution** — how many of your agents are Online vs. Busy vs. Offline

* **Conversation traffic heatmap** — a day-of-week × hour-of-day grid showing when new conversations land

* **Resolution heatmap** — same grid, but showing when conversations get resolved

* **Team-level conversation counts** with optional team filter

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSmRUSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--4b9fea7ca635f80bb9101a5a5b1bf2cb8c5a3aac/overview-reports.jpg)

***What to do with it:** open it on a wall display for the team room. Use the heatmap to figure out staffing — if Tuesday 2pm is your busiest hour and Friday morning is dead, that's where shift planning starts.*

### 2. Conversation Reports

**Question it answers:** *"How is the whole operation trending?"*

\
![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCUDFUSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--9356ae12f36dd2238e415344cd26526a89bd6f20/conversations-reports.jpg)

Account-wide totals for the six core metrics, plotted over time. This is the report you check weekly to spot trends, climbing reply times, growing volume, dropping resolution counts.

### 3. Agent Reports

**Question it answers:** *"How is each agent performing?"*

Same six metrics, scoped to one agent at a time. Pick an agent from the filter dropdown and see their personal numbers over the chosen window.

***A word of caution:** agent metrics measure workload-weighted output, not effort. An agent handling complex enterprise tickets will look "slower" than one fielding password-reset volume. Always read these alongside CSAT and conversation context, never as a standalone score.*

### 4. Inbox Reports

**Question it answers:** *"Which channel needs more love?"*

Same metrics, scoped to one inbox. This is how you compare email vs. live chat vs. WhatsApp on response times and volume and find the channel that's lagging.

### 5. Team Reports

**Question it answers:** *"How is each team performing?"*

Same metrics, scoped to one team (Engineering, Billing, Customer Success, etc.). Useful when teams own different conversation types and "average across the company" hides the picture.

### 6. Label Reports

**Question it answers:** *"What kinds of conversations are taking the longest?"*

Same metrics, scoped to one label. If you've been disciplined about labelling (Lesson 3a), this is where you find the gold:

* *Are `bug-report` conversations resolving slower than `billing`?*

* *Has `feature-request` volume been growing?*

* *Is `vip` conversation reply time within target?*

*Label reports are only as good as your label hygiene. If your team labels inconsistently, this report will mislead.*

### 7. CSAT Reports

**Question it answers:** *"Are customers actually happy?"*

CSAT surveys are sent to customers when their conversation is resolved (if enabled on the inbox). They're a 5-star scale.

The report shows:

* **Total responses received**

* **Satisfaction score** — the percentage of responses that were 4 or 5 stars

* **Response rate** — the percentage of surveys that got a reply

* **Rating distribution** — how the responses break down across 1–5 stars

* **Individual responses** — table of each survey response with the conversation, agent, inbox, rating, and any feedback text

You can filter by agent, inbox, team, or specific rating — useful for finding all the 1-star feedback and reading it directly.

### 8. SLA Reports

**Question it answers:** *"Are we keeping the promises we made?"*

If you set up SLAs in Lesson 4, this is where you see how you're doing.

* **Hit rate** — what percentage of conversations met the SLA targets

* **Breach count** — how many missed

* **Total conversations in scope** — the denominator

* **Per-conversation table** — every SLA-tracked conversation with its policy, assigned agent, and hit/breach status with timestamps

Filters: agent, inbox, team, SLA policy, labels. Full CSV export.

> **The "why" matters more than the number.** A 92% hit rate is fine; the 8% breach list is where you go to investigate. Sort by oldest breach and read the top ten — patterns will jump out (one agent, one inbox, one time of day).

### 9. Bot Reports

**Question it answers:** *"Is the bot actually helping?"*

For accounts using bots or AI assistants:

* **Bot resolutions** — conversations the bot resolved without human handoff

* **Bot handoffs** — conversations the bot escalated to a human agent

A healthy ratio depends on your strategy. Some teams want a high resolution rate (bot handles common questions); others want a high handoff rate (bot is just triage). Decide what you're aiming for before judging the numbers.

---

## Common questions

**Why does my agent report show zero conversations even though I've been replying?**

Agent metrics attribute conversations to the assignee at resolution time. If you replied but the conversation was assigned to someone else (or unassigned), it doesn't roll up to you. Make sure conversations are assigned correctly.

**Can I schedule reports to be emailed weekly?**

Not natively, no. The CSV export is the official path for offline / scheduled use, combine it with a scheduler you use elsewhere.

**What's the difference between "Resolutions Count" and "Conversations Created"?**

Different conversations. *Created* counts conversations that *started* in the window. *Resolutions* counts conversations that were *resolved* in the window, they may have been created weeks earlier. The two numbers should be close in steady state; a big gap signals backlog growing or shrinking.

---

## What's next

You've now covered every layer of running an operation in Chatwoot — from your first reply (Lesson 1), through the manual toolkit, automation, AI, and the metrics that tell you whether the whole thing is working (this lesson). That's the full operating loop: handle, automate, augment, measure.
