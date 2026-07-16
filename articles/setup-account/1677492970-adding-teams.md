# A complete guide to teams in Chatwoot

A **team** is a group of agents in your account, organized around a shared responsibility — for example, a Sales team, a Support team, or an Engineering team. Teams are an account-level concept: they live across inboxes, and a single agent can belong to as many teams as makes sense.

You use teams when you want to route a conversation to *a group of agents*, not a specific person — so that anyone on the right team can pick it up. Common patterns:

* "Send all billing questions to the Finance team."

* "Anything from Enterprise customers goes to the Senior Support team."

* "Bug reports get routed to Engineering."

A team has three things:

* A **name** (required, unique within your account)

* An optional **description**

* An **auto-assign** toggle that controls whether conversations sent to the team are automatically distributed to a member, or left for someone to pick up manually

A conversation can have **both** a team and an individual assignee. The team scopes *who* can be auto-assigned; the assignee is the one specific agent currently responsible for the reply. Either, both, or neither can be set on a conversation at any time.

***Permissions:** only **administrators** can create, edit, or delete teams. Regular agents can see the list of teams and the conversations assigned to teams they belong to, but cannot manage teams.* 

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTWVTSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--814128187fae33803cc3afda06ce63d6f25eaba3/teams.jpg)

## Managing teams

### Creating a team

Creating a team is a three-step wizard.

**Step 1 — Open the create flow.**

Go to **Settings → Teams** and click **Create new team** in the top-right of the page.

**Step 2 — Set the basics.**

Fill in the form:

| Field                               | What it's for                                                                                                                                                                                  |
| ----------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Team Name**                       | A short, recognizable name. E.g. *Sales*, *Support*, *Engineering*. Required and must be unique in your account.                                                                               |
| **Team Description**                | A one-line description of what the team handles. E.g. *"Resolves queries related to sales of Hopkins products."*                                                                               |
| **Allow auto assign for this team** | When ticked, conversations assigned to this team are automatically distributed to its agents. When unticked, conversations stay in the team's queue as unassigned until someone picks them up. |

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQWVVSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--7db0a3a777ea3ea42e0f4e66bc7de86d979cc944/add-team.jpg)

Click **Create team**.

**Step 3 — Add agents.**

Pick the agents who should be members of this team. Tick the checkbox next to each agent and click **Add agents**. Only agents you add here will see the team's conversations and be eligible for auto-assignment from it.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQW1WSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--74e60a8439165e69fb1be68a7602364d9334eb5c/add-agents-to-team.jpg)

**Step 4 — Finish.**

Click **Finish** on the confirmation screen. Your new team appears in the team list at **Settings → Teams**.

---

### Editing a team

1. Go to **Settings → Teams**.

2. Find the team you want to edit and click the **settings icon** next to it — two horizontal sliders (tooltip: *Edit team*).

3. You'll be taken back through the same multi-step flow used during creation:

   * **Edit the basics** — change the name, description, or auto-assign setting. Click **Update team**.

   * **Edit agents** — add or remove members by ticking/unticking the checkboxes. Click **Update agents in team**.

   * **Finish** — confirm the changes.

To discard changes mid-flow, use the **Back** button at the top-left of the screen.

---

### Deleting a team

1. Go to **Settings → Teams**.

2. Find the team you want to delete and click the **trash (bin) icon** next to it (tooltip: *Delete*). The icon turns red on hover.

3. A confirmation modal appears with the title *"Are you sure you want to delete the team?"* and the message *"Deleting the team will remove the team assignment from the conversations assigned to this team."*

4. **Type the team's name into the confirmation field** — this is required to enable the delete button. Then click **Delete <team name>** to confirm, or **Cancel** to back out.

**What happens to existing conversations when you delete a team?**

The conversations themselves are *not* deleted — but their **team assignment is cleared**. Each conversation that was assigned to the deleted team will simply have no team going forward; their individual assignees and other attributes are unchanged. If you want the conversations re-routed to a different team, do that *before* deleting.

> **Note:** there's no requirement that a team be empty before deletion. You can delete a team that still has agents assigned to it — the agents just lose their membership; their user accounts stay intact.

---

## How to use teams

Once a team exists, it becomes available almost everywhere conversations get routed, filtered, or analyzed. Here's the full set of places you can use a team in Chatwoot.

### 1. Assign a conversation to a team

The most direct use. Open any conversation, find the **Team** field in the conversation actions panel on the right sidebar, and pick a team from the dropdown.

* If the team has **auto-assign enabled**, an agent on that team is picked automatically and becomes the assignee.

* If the conversation has an existing assignee who is *not* a member of the new team, the assignee is cleared so auto-assignment can pick a valid one.

* If auto-assign is off, the conversation stays unassigned but is now scoped to the team — anyone on the team can pick it up.

You can change or remove the team at any time from the same dropdown.

### 2. Assign teams in bulk

In the conversation list, select multiple conversations using the checkboxes and use the bulk action bar at the top to **assign a team** to all of them at once. Useful during incidents — bulk-route every affected conversation to the team that owns the fix.

### 3. Filter conversations by team

In the conversation list, you can narrow what you see to a specific team:

* Use the **Team** filter in the conversation list filter panel.

* Or save a folder with a team condition for one-click access.

Common saved folders worth building:

* *My team's open queue* — Team = *Support*, Status = *Open*

* *Engineering bugs* — Team = *Engineering*, Label = `bug-report`

* *Unassigned in my team* — Team = *Support*, Assignee = *None*

### 4. Use teams in automation rules

Automation rules integrate with teams in two ways:

* **As a condition** — *"If team is Engineering, do X."*

* **As an action** — *"Assign team Engineering"*, or *"Remove assigned team."*

This is how you wire up rules like:

* *"Any conversation containing the word `invoice` → assign team Finance."*

* *"Any conversation labeled `vip` → assign team Senior Support and set priority High."*

### 5. Use teams in macros

When building a macro, the action picker offers:

* **Assign Team** — set the team

* **Remove Assigned Team** — clear it

So a macro like *Escalate to engineering* can in one click: assign team *Engineering*, set priority *High*, add label `escalated`, and send a templated message.

### 6. Filter and scope reports

Under **Reports → Team**, you get a dedicated **Team Report** that shows the six core metrics (Conversations Created, Incoming Messages, Outgoing Messages, Avg First Response Time, Avg Resolution Time, Resolutions Count) scoped to a single team. Pick a team from the filter, set a date range, and you're comparing team-level performance with the same toolkit as inboxes and agents.

CSAT and SLA reports also accept a team filter, so you can answer:

* *"How does Engineering's CSAT compare to Support's?"*

* *"How often is the Senior Support team breaching SLA?"*

---

## How teams interact with inboxes and assignees

It's easy to mix these three concepts up. The difference matters:

| Concept      | Scope            | What it controls                                                            |
| ------------ | ---------------- | --------------------------------------------------------------------------- |
| **Inbox**    | Per channel      | Which agents *can* see and reply to conversations on that channel           |
| **Team**     | Account-wide     | Which agents *should* handle a conversation, used for routing and reporting |
| **Assignee** | Per conversation | Which one specific agent is currently responsible for replying              |

---

## Frequently asked questions

**Can an agent be in multiple teams?**

Yes. Agents can belong to as many teams as you want. A single agent can be in *Support*, *Engineering*, and *VIP Response* simultaneously.

**Can a conversation belong to multiple teams?**

No. A conversation has at most one team at a time. If you need multi-team awareness, use **labels** alongside team assignment.

**What happens if I turn auto-assign off?**

New conversations assigned to the team after the change won't be auto-distributed; they'll wait in the team's unassigned queue. Existing assignments are unaffected.

**If I remove an agent from a team, what happens to their conversations?**

Conversations they were already assigned to stay assigned to them — being removed from the team doesn't yank existing work. New auto-assignments in that team will skip them.

**Can a non-admin create or edit a team?**

No. Team management is administrator-only. Non-admins can see teams and work on team-assigned conversations, but cannot modify the team list or membership.

**Why does the assignee disappear when I switch a conversation's team?**

If the current assignee isn't a member of the new team, Chatwoot clears the assignee so auto-assignment can pick a valid team member. This prevents conversations being "stuck" with an agent who no longer belongs to the responsible team.

**Are deleted teams recoverable?**

No. Team deletion is permanent. The conversations survive (with their team field cleared) but the team record itself is gone. Re-create it with the same name if needed, but it's a brand-new team.

**Is there a limit on how many teams I can create?**

There's no hard cap in the product. Practical advice: keep the count small enough that the team list fits on one screen. If you find yourself with twenty teams, you've probably split too finely.
