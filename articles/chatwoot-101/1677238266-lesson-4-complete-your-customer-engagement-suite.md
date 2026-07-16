# Lesson 4: Automation and Routing

So far, every action you've taken in Chatwoot has been *manual*, you clicked, you typed, you assigned. That works for 10 conversations a day. It collapses at a hundred.

This lesson is about the systems that run *while you sleep*: business hours, auto-assignment, automation rules, and SLAs. Set these up once, and the dashboard does the routine work for you, landing the right conversation on the right agent at the right time, with the right urgency, before anyone has to think about it.

## What you'll learn

* When to automate something and when not to

* How to set business hours so customers know what to expect outside working time

* How to auto-assign conversations to agents using assignment policies

* How to write automation rules that label, route, and reply based on conditions

* How SLAs put a clock on response and resolution times, and what happens when one's about to breach

* How all four systems chain together to handle volume gracefully

**You'll need:** Admin access to your Chatwoot account. Most of this lesson lives under **Settings**, which agents typically can't edit.

---

## A mindset before we start: when to automate

Automation feels powerful, and that's the trap. The temptation is to automate *everything* on day one and end up with a tangle of rules that fight each other six months later.

A simple test before you build any rule:

> *"Have I done this exact same thing manually at least ten times in the last two weeks?"*

If yes, it's worth automating. If no, do it manually a few more times until you're sure of the pattern. Bad automation is worse than no automation — it routes things wrong, replies inappropriately, and erodes trust in the system.

Build slow. Delete aggressively. Review your rules quarterly.

---

## 1. Business Hours — telling customers when you're around

**Business Hours** define when your team is available, per inbox. They power three things:

1. **Out-of-hours messages.** Customers who write outside business hours see a custom message ("We're back at 9am EST tomorrow") instead of nothing.

2. **SLA timers.** When SLAs are configured to use business hours, the clock pauses overnight and on weekends — so a Friday-evening ticket isn't already 2 days "late" when Monday morning starts.

3. **Reporting accuracy.** Response time metrics can be calculated against working time, not wall-clock time.

   

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCUGxTSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--43588d1cae647bd56851e8ed0c238d67c03943c4/business-hours.jpg)

### Setting them up

1. Go to **Settings → Inboxes**, click your inbox, then the **Business Hours** tab.

2. Toggle **Enable business availability for this inbox**.

3. Pick your **timezone**.

4. For each day of the week, set the **start and end times** (or mark the day as unavailable).

5. Write your **out-of-office message** — keep it short and warm: *"Thanks for reaching out! Our team is available Mon–Fri, 9am–6pm EST. We'll get back to you first thing tomorrow."*

6. Save.

---

## 2. Auto-assignment — who gets the next conversation

By default, new conversations land in **Unassigned** and an agent has to grab them. Good for tiny teams. Painful at any real volume.

Chatwoot's auto-assignment picks an agent for each new conversation automatically. Two strategies:

### Round Robin

The default. Conversations are distributed evenly across all online, available agents in the inbox. Simple, fair, and what most teams should start with.

### Balanced Assignment

Distributes based on *current load* — the agent with the fewest open conversations gets the next one. Better for teams where some conversations take much longer than others.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRnBSSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--2c16ca433ba19420c7661a8c55f3a142dd97b47c/conversation-assignment.jpg)

### Setting it up

1. **Settings → Inboxes →** your inbox **→ Configuration**.

2. You will see an option to configure an assignment policy.

3. Save.

### What auto-assignment respects

* **Agent availability.** Offline and Busy agents are skipped (Busy can be configured per workspace).

* **Inbox membership.** Only agents added to that specific inbox are eligible.

* **Capacity** (Enterprise / Custom Roles). You can cap how many open conversations one agent can hold at once.

***Tip:** Auto-assignment routes the conversation initially. Reassignments (manual or via macro) override it. So you can let the system pick a default, and let humans intervene when context demands.*

---

## 3. Automation Rules — the if-this-then-that engine

If business hours and auto-assignment handle *every* conversation the same way, **automation rules** handle *specific* conversations specifically. They're the rule engine that listens for events, checks conditions, and runs actions.

\
![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTWRSSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--964768f871243d2495cd203472108b54f27cabd5/automation-rule.jpg)

### Anatomy of a rule

Every automation rule has three parts:

1. **Event** — when does the rule consider firing?

   * *Conversation Created* — runs once, when the conversation first appears

   * *Conversation Updated/Opened/Resolved* — runs when something changes (status, assignee, label, custom attribute)

   * *Message Created* — runs on each new incoming or outgoing message

2. **Conditions** — who does it apply to? Filters on inbox, channel, content, contact attributes, custom attributes, business hours, etc.

3. **Actions** — what should happen? Assign agent or team, add labels, send messages, change status, run a macro, etc.

### Setting one up

**Settings → Automation → Add Automation Rule.**

Name it, pick the event, build the conditions (combinable with `AND`/`OR`), pick the actions (you can chain several), and save. Rules run in the order they're listed.

### Some rules worth building first

| Rule name                 | Event                | Condition                                      | Actions                                                  |
| ------------------------- | -------------------- | ---------------------------------------------- | -------------------------------------------------------- |
| **Route billing tickets** | Conversation Created | Message contains *invoice*, *charge*, *refund* | Assign Team *Finance*; add label `billing`               |
| **Flag VIPs**             | Conversation Created | Contact attribute *Plan* = `Enterprise`        | Set Priority *High*; add label `vip`; assign senior team |

### Common pitfalls

* **Loops.** A rule that sends a message, listening for *Message Created*, can re-trigger itself. We would not run automations on actions that were triggered by another automation. Always scope conditions tightly to avoid this.

* **Silent rules.** It's easy to forget a rule exists. Make sure that you are checking the automation rules once every quarter to see if you should update something.

***Macros vs. Automation Rules:** macros are manual, you click and run. Automation rules are automatic, they run on events. When you find yourself running the same macro on every conversation matching a pattern, convert it to an automation rule.*

---

## 4. SLAs — putting a clock on response

An **SLA (Service Level Agreement)** is a policy that says *"this kind of conversation must get a response within X minutes and a resolution within Y hours."* Chatwoot tracks the clock for you, surfaces conversations that are about to breach, and reports on how often you hit your targets.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRVpTSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--9776526c8c098690df1023dfb67d6cd094092935/sla.jpg)

### The three timers an SLA can track

* **First Response Time (FRT)** — how long until the *first* agent reply

* **Next Response Time (NRT)** — how long until each *subsequent* reply when the customer is waiting

* **Resolution Time (RT)** — how long until the conversation reaches *Resolved*

You can set any combination, with different thresholds.

### Setting one up

1. **Settings → SLA → Add SLA**.

2. Name it (e.g. *Enterprise priority*).

3. Set the targets — *FRT: 15 min*, *NRT: 30 min*, *RT: 4 hours*.

4. Choose whether the clock uses **business hours** or runs 24/7.

5. Save.

### Applying it to conversations

SLAs aren't applied to every conversation by default — that would be noise. Apply them via Automation rule.

### What you see on the dashboard

* A **countdown** on conversations with an active SLA, in the conversation list and the conversation header.

* An **SLA breach indicator** when a target has been missed.

* A **dedicated SLA report** showing hit rate, breach reasons, and trends.

***Don't over-promise.** A 5-minute FRT SLA on every inbox sounds great until you breach it 80% of the time. Pick targets you can actually hit, and tighten as the team gets faster.*

---

## 5. How they all chain together

Here's a Tuesday-morning customer message flowing through the whole system, with no manual touch until step 7:

1. **9:03am.** A customer on the Enterprise plan writes in via the website widget: *"Our exports are failing again."*

2. **Business Hours** check — yes, we're open. No auto-responder fires.

3. **Auto-assignment (Round Robin)** picks Sarah, who's online.

4. **Automation rule "Flag VIPs"** matches: contact's `Plan` = `Enterprise`. Sets priority *High*, adds label `vip`, applies the *Enterprise priority* SLA.

5. **Automation rule "Route bug reports"** matches the word `failing`. Adds label `bug-report`.

6. **SLA timer starts.** FRT countdown: 15:00.

7. **Sarah opens the conversation.** Everything she needs is already in place — priority set, labels applied, engineer looped in, countdown showing 14:42 left. She replies in two minutes.

8. **SLA stops the FRT clock** at 02:18 — well within target.

What you'd otherwise do manually, read the contact panel, set priority, label, loop in engineering, mentally start a clock, has all happened before Sarah even saw the conversation.

That's the whole point.

---

## Mini-exercise (8 minutes)

You'll need admin access. We'll build a small-but-real automated workflow.

1. **Set business hours** on your test inbox: Mon–Fri, 9am–6pm in your timezone, with a friendly out-of-office message.

2. **Enable auto-assignment** with Round Robin. Add yourself as the only agent so you get every conversation.

3. **Build an automation rule:**

   * Event: *Conversation Created*

   * Condition: *Message contains* `bug`

   * Actions: *Add label* `bug-report`, *Set priority* `High`

4. **Build an SLA**: name it *Standard*, FRT = 30 min, RT = 24 hours, business hours on.

5. Apply the SLA to your test inbox by default.

6. **Test it.** Open the widget and send the message *"I think I found a bug"*.

7. Check the resulting conversation: it should be auto-assigned to you, labeled `bug-report`, priority High, with an SLA countdown ticking.

If all four pieces fired, you've automated more than most teams ever do.

---

## Common questions

**Will an automation rule run on conversations that already exist?**

No — rules run forward. They only fire on events that happen *after* you create or enable the rule. Existing conversations are unaffected.

**Can I disable a rule temporarily without deleting it?**

Yes. Each rule has an **Active** toggle in the automation list. Use this for seasonal rules ("Holiday autoresponder") that you want to keep configured but turn off most of the year.

**What happens if two rules both match the same conversation?**

Both run, in the order they're listed. Watch out for conflicting actions (e.g. one rule assigns Team A and another assigns Team B — last write wins).

**Do SLAs apply on weekends?**

Only if you've configured the SLA to ignore business hours. Default behavior pauses the clock outside working hours so you don't breach overnight.

**Can a customer see their SLA timer?**

No. SLA countdowns are agent-facing only. The customer just experiences faster responses.

**Does auto-assignment skip an agent if they're at capacity?**

Yes, when you've set capacity limits via Custom Roles or workspace config. Otherwise it distributes regardless of current load (Round Robin) or by load (Balanced).

##
