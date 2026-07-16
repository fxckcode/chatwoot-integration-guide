# Setting per-agent conversation caps with Agent Capacity Policies

An **Agent Capacity Policy** is a bundle of rules that caps how many open conversations a single agent can hold at a time. It's how you stop one agent from drowning while another sits idle, and how you keep auto-assignment fair when conversation volumes spike.

When auto-assignment looks for an eligible agent, it checks each candidate's capacity policy (if they have one) before assigning. Agents at or over their cap are skipped; the next eligible agent under cap is assigned instead.

A policy has:

* A **name** (required)

* An optional **description**

* A set of **per-inbox capacity limits** — different caps per inbox if you want

* Optional **exclusion rules** — labels and conversation age that should be ignored when counting open conversations

*Permissions: only administrators can create, edit, or delete capacity policies, and only admins can attach them to agents.*

---

## Managing capacity policies

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTG0ySXdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--a78dd13ca35419d59d4a1db3869312b7b67f8395/agent-capacity.jpg)

### How to create a capacity policy?

1. Go to **Settings → Agent Capacity** and click **Create agent capacity policy**.

2. Fill in:

   * **Policy name** — required, max 255 characters.

   * **Description** — optional.

   * **Inbox capacity limits** — for each inbox you want to cap, set a maximum number of open conversations an agent under this policy can hold on that inbox.

   * **Exclusion rules** (optional):

     * **Excluded labels** — conversations with these labels don't count toward the cap.

     * **Exclude older than** — conversations older than N hours don't count toward the cap.

3. Add the agents who should be governed by this policy under **Assigned agents**.

4. Save.

### How to edit a capacity policy?

1. Go to **Settings → Agent Capacity** and open the policy.

2. Change the limits, exclusions, or assigned agents.

3. Save.

### Delete a capacity policy

Deleting a policy unassigns it from every agent. The agents revert to having no cap and become eligible for unrestricted auto-assignment.

---

## How exclusion rules work

The point of exclusions is to make caps measure *real, active workload* — not just any open conversation that happens to still exist.

### Excluded labels

Add labels like `waiting-on-customer` or `parked` to the exclusion list. Conversations with those labels still belong to the agent but don't count toward the cap. So if your cap is 10 and an agent has 7 active + 5 `waiting-on-customer`, they still have capacity for 3 new ones.

### Age exclusion

Set "exclude older than 24 hours" and conversations created more than a day ago drop out of the count. Useful for long-running conversations (e.g. multi-day enterprise tickets) that you don't want monopolizing an agent's capacity number.

***Tip:** start with a generous cap and no exclusions. Add exclusions only when you can point to a specific kind of conversation that's distorting the count.*

---

## How to attach a policy to an agent?

You can attach the policy when creating it (under **Assigned agents** in the policy form) or after the fact:

1. Open the policy.

2. Click **Add agent**.

3. Pick the agents you want under this policy. Multiple agents can share one policy.

A given agent can be on at most one capacity policy at a time. Assigning a new policy replaces any prior one.

---

## How auto-assignment uses capacity?

When a new conversation arrives in an inbox with auto-assignment enabled:

1. Chatwoot finds eligible agents (inbox members, available status).

2. For each candidate with a capacity policy, count their currently-open conversations on that inbox, applying exclusion rules.

3. Filter out agents at or over their cap.

4. Pick the next eligible agent using the configured assignment strategy (Round Robin or Balanced).

If no agent is under cap, the conversation stays unassigned in the queue until somebody's count drops or capacity frees up.

*Capacity is **per inbox**. An agent can be at cap on Inbox A while still having capacity on Inbox B — they'll be skipped for A but eligible for B.*

---

## A practical example

A 12-agent support team has these inboxes:

* **Website** — high volume, short conversations

* **Email** — lower volume, longer conversations

You create two capacity policies:

| Policy | Website cap | Email cap | 
|--------|-------------|-----------| 
| **Standard agent** | 10 | 5 | 
| **Senior agent** | 15 | 8 |

Junior agents go on *Standard*; senior agents on *Senior*. Add exclusion: `waiting-on-customer` (so parked conversations don't count). Add age exclusion: 48 hours (so a week-old enterprise email isn't blocking an agent's slot).

The result: traffic gets distributed without any single agent being overwhelmed, and the senior team takes a heavier share without manual intervention.

---

## Frequently asked questions

**What happens to a conversation that's already assigned when an agent hits their cap?**

Nothing. Caps only affect *new* auto-assignments. Existing assignments stay put.

**Can an agent reassign a conversation away to free up capacity?**

Yes — manual reassignment works as normal. If you reassign a conversation to a teammate, your open count drops by one and the next inbound auto-assignment can target you again.

**What if every agent is at cap?**

The conversation stays unassigned in the queue until somebody's count drops (a conversation gets resolved, snoozed, or reassigned). Pair this with monitoring of unassigned-queue length — if it grows, you need either more headcount or a higher cap.

**Can I set per-team capacity?**

Capacity is configured per agent, not per team. To approximate team capacity, attach the same capacity policy to every agent on the team.

**Are exclusions applied at the agent level or the policy level?**

Policy level. All agents on a given policy share the same exclusion rules.
