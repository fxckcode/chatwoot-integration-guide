# Lesson 5: AI Actions

[Lesson 4](https://www.chatwoot.com/hc/user-guide/articles/1677238266-lesson-4-complete-your-customer-engagement-suite) was about *rules* — if-this-then-that automation that runs without judgment. This lesson is about *AI* — the layer that brings judgment, language, and reasoning into your support stack.

Captain, the AI Agent in Chatwoot doesn't just route conversations; it can read them, understand them, look up answers, and act on your behalf.

There are two parts, and they do different jobs:

* **Captain AI Assistant**: customer-facing AI that handles conversations on behalf of your team.

* **Captain Copilot** : agent-facing AI that helps *you* handle conversations faster.

This lesson covers both, plus the actions Captain can take inside your account.

## What you'll learn

* The difference between Captain and Copilot, and when to reach for each

* How to configure a Captain Assistant — knowledge, guardrails, response guidelines, behavior toggles

* The seven built-in actions an Assistant can take inside Chatwoot

* How custom tools let an Assistant call your APIs

* How scenarios route conversations through conditional handoff workflows

* How Copilot helps an agent inside a single conversation

* The limits and guardrails worth understanding before you go live

**You'll need:** An account with the Captain feature enabled. Captain is a premium, Enterprise-gated capability — if you don't see the Captain icon in the navigation rail, the feature isn't enabled on your plan/install. You'll also need to provide an OpenAI key at the system level (handled by your installation admin).

Before we go anywhere, here is the mental model:

|                      | **Captain**                                                 | **Copilot**                                                   |
| -------------------- | ----------------------------------------------------------- | ------------------------------------------------------------- |
| Who it talks to      | Your customer                                               | Your agent                                                    |
| Where it appears     | Inside the chat widget / inbox                              | In the conversation sidebar, message editor, bulk actions     |
| What it does         | Handles the conversation directly, with handoff when needed | Suggests replies, answers agent questions, surfaces knowledge |
| Visible to customer? | Yes, they're chatting with it                               | No, internal use only                                         |
| Goal                 | Deflect / resolve without a human                           | Help the human be faster                                      |

You can use one, the other, or both. Most teams start with Copilot and build AI Assistant on specific inboxes once they have visibility of the things that should automate.

---

## 1. Captain Assistants — the configurable AI

A **Captain Assistant** is a named, configurable AI persona. You can create multiple Assistants — for example, a support Assistant for the website inbox and a sales Assistant for the WhatsApp inbox.

### Configuring an Assistant

Go to **Captain** in the navigation and create a new Assistant. You'll set:

* **Name & description** — for your team's reference

* **Product name** — used in prompts so the AI talks about *your* product, not "the product"

* **Temperature** — how creative vs. deterministic the responses should be (lower = more predictable, higher = more varied)

* **Feature toggles**:

  * **FAQ lookup** — let the Assistant search your knowledge base before replying

  * **Conversation memory** — let it consider earlier messages in the same conversation

  * **Contact attributes** — let it factor in what you know about the contact (plan, signup date, etc.)

***Tip:** start with a tightly scoped Assistant. "Answer questions about our pricing and refund policy. If asked anything else, hand off to a human." A narrow scope produces good results fast and earns trust. Widen later.*

### Connecting an Assistant to an inbox

An Assistant only handles customer conversations on inboxes you explicitly connect it to. From the Assistant's settings, choose which inboxes it should engage with. Conversations on those inboxes will be handled by the Assistant first; everywhere else stays human-only.

***Recommended starting point:** create one Assistant, connect it to one low-stakes inbox (FAQ-style queries, not billing or technical bugs), and watch how it does for a week before expanding.*

---

## 2. Knowledge — what the Assistant knows

Out of the box, the Assistant knows nothing about your business. You feed it knowledge through **documents**.

### Three types of knowledge sources

| Type     | What it is                                               | Limit                   |
| -------- | -------------------------------------------------------- | ----------------------- |
| **URL**  | Crawl a public webpage (your docs, marketing site, blog) | Per-plan document quota |
| **PDF**  | Upload a file (manuals, internal docs, policies)         | 10MB per file           |
| **Text** | Paste raw text directly                                  |                         |

When you add a document, Captain processes it into internal embeddings — a searchable representation. You'll see a status of *syncing* → *synced* (or *failed*). Once synced, the FAQ lookup tool can pull from it during conversations.

### What to put in (and what to leave out)

**Good knowledge:**

* Help Center articles

* Pricing pages

* Refund / shipping / cancellation policies

* Onboarding docs

**Bad knowledge:**

* Internal Slack threads (irrelevant chatter)

* Blog posts about company values (won't help solve a support ticket)

* Outdated docs (the AI will confidently quote them — keep your knowledge fresh)

***Garbage in, garbage out:** the Assistant is only as accurate as your documents. Audit and re-sync regularly. If your refund policy changed in March and the synced PDF still says February, the AI will tell customers the wrong thing.*

---

## 3. Actions — what an Assistant can *do*

This is where Captain stops being a chatbot and starts being an agent. An Assistant can take **actions** inside your Chatwoot account — not just talk.

### Built-in actions

| Action                             | What it does                                                    |
| ---------------------------------- | --------------------------------------------------------------- |
| **FAQ Lookup**                     | Search synced documents for relevant content                    |
| **Handoff to Human**               | Route the conversation to a human agent                         |
| **Add Contact Note (coming soon)** | Write a note on the contact's profile                           |
| **Add Private Note (coming soon)** | Drop an internal note in the conversation                       |
| **Update Priority (coming soon)**  | Set the conversation priority (Low / Medium / High / Urgent)    |
| **Add Label (coming soon)**        | Apply a label to the conversation                               |
| **Resolve Conversation**           | Close the conversation when the customer's question is answered |

The Assistant decides which action to take based on the conversation. It might answer a pricing question via FAQ Lookup, then add a `pricing-inquiry` label, then resolve. Or it might recognize an angry customer, set Priority to High, write a private note summarizing the issue, and hand off.

### Custom tools — calling your own APIs

For anything beyond the built-ins, you can define **custom tools**: HTTP endpoints the Assistant can call. Each custom tool is:

* A name and description

* An HTTP **GET** or **POST** request to a URL you control

* A **parameter schema** (what inputs the AI should fill in)

* **Authentication** — Bearer token, Basic, or API key

* Optional **request/response templates** for shaping the data

This is how you wire Captain into your own systems. Examples:

* *"Look up the customer's order status"* → POST to your orders API

* *"Check inventory for SKU X"* → GET to your inventory service

* *"Issue a credit"* → POST to your billing system

Custom tools are gated behind their own feature flag and capped at 15 per account. Treat that limit as a feature — it forces you to think about which tools really earn their place.

***Security note:** the AI will call any tool you define. Scope tools tightly: read-only where possible, idempotent where not, and never expose actions whose blast radius you wouldn't trust to a brand-new agent.*

---

## 4. Copilot — the agent's AI sidekick

Copilot lives inside the conversation interface, on the agent's screen, and only the agent sees it.

### What Copilot does

Open any conversation and look for the Copilot panel. You can:

* **Ask questions about the conversation** — *"What is this customer asking for?"*, *"What's the right next step here?"*

* **Get reply suggestions** — Copilot drafts a response based on the conversation history and your knowledge base, and offers a USE button that drops the suggestion straight into your reply box.

* **Search your knowledge base in natural language** — instead of remembering exact phrasing.

Each Copilot conversation is a *thread* tied to the underlying Captain Assistant — so Copilot uses the same knowledge, guardrails, and response guidelines. Configure your Assistant well and Copilot benefits automatically.

### How it differs from Captain in practice

Captain replies to the customer directly. Copilot drafts something the agent reviews, edits, and decides whether to send. The agent stays in the loop. For most teams, this is a much safer place to start with AI.

***Practical workflow:** treat Copilot's suggestions as a first draft, not a final reply. Read it, edit it, personalize it. The minute you start sending Copilot output verbatim, your replies start sounding like everyone else's.*

---

## Captain vs. Agent Bots — quick clarification

Chatwoot has had **Agent Bots** for a long time — webhook-based bots that handle the start of a conversation and hand off. Agent Bots are open-source, free, and *not* AI. They're rule-driven, scripted bots.

**Agent Bots** = scripted, OSS, free, deterministic.

**Captain Assistants** = AI, Enterprise, premium, language-driven.

Most new accounts will want Captain. Agent Bots are still useful for simple deterministic flows (collecting an email, gating a conversation behind a few questions).

---

## How it all fits together (a worked example)

A customer messages your website widget at 2am: *"How do I cancel my subscription?"*

1. The widget is connected to an inbox where Captain is enabled.

2. Captain reads the message, runs **FAQ Lookup**, and finds the cancellation policy in your synced docs and replies.

3. The customer replies. Captain calls a **custom tool** `lookup-account` with that email and gets back the account status.

4. Captain confirms the account, walks the customer through the cancellation, applies the **`cancellation`** label, sets **Priority** = `Low`, and **Resolves** the conversation.

5. The next morning, your team sees a clean resolved conversation with a private note Captain wrote summarizing the interaction. Reports show a deflected ticket. The customer got an answer at 2am instead of waiting twelve hours.

That's the whole AI promise in one example. Set up well, it's transformative.

---

## Common questions

**Will Captain reply to every message on connected inboxes?**

Yes — that's the design. Captain engages with incoming conversations on inboxes it's connected to. If you only want it on certain conversations, you'd handle that with inbox separation.

**Can I review Captain's replies before they go to the customer?**

Not natively. Captain replies directly. If you want a human-in-the-loop pattern, use Copilot instead — agent drafts with AI assistance, agent sends.

**Does Captain learn from conversations?**

Memories feature in Captain suggests the knowledge gaps from the conversation. You can approve the generated FAQs so that the knowledge of Captain updates regularly.

**What happens when Captain doesn't know the answer?**

It will collect some additional information depending on the context and will Handoff to Human.

**Is the customer told they're talking to AI?**

That's a product/policy choice on your side. There's no enforced disclosure. Many teams configure their welcome message to say something like *"I'm Acme's AI support assistant — I can resolve common questions instantly, or hand you to a human anytime."*

**Can custom tools have side effects (write actions)?**

Yes — POST endpoints can mutate state. This is how you let the Captain cancel subscriptions, issue credits, etc. Treat write tools the same way you'd treat handing a junior agent a write-enabled API key: scope tightly, log everything, and put irreversible actions behind a confirmation step in your scenario.

**My account doesn't have Captain. Can I get it?**

Captain is gated to paid plans only. If you're self-hosting, you can enable it on premium support plans or higher.
