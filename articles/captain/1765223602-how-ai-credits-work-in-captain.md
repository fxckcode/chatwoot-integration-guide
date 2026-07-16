# How AI Credits work in Captain?

This guide explains how AI credits are consumed, how your credits are updated when you top up, when your monthly renewal happens, what happens when you change plans, and how notifications work if your credits run out.

## How are AI credits consumed?

AI credits are deducted whenever an AI action is performed. Examples include:

* Captain assistant responses

* Copilot lookups

* Editor actions (rephrase, summarise, suggest a reply)

* Label Suggestions

* Any workflow or automation that triggers a model call

* Audio transcription

Different models consume credits at different rates. At the moment, **all actions consume 1 credit per message**, since a fixed model configuration only is supported.

This will change in the future as more model options are supported, at which point different models may consume different credit amounts per action.

If an action cannot be completed due to insufficient credits, a credit failure occurs (explained later).

## **When does usage reset?**

Usage resets to 0 only during monthly renewal.   
  
Usage does NOT reset when: 

* Topping up credits

* Changing your plan

* Changing seat count

This means you can top up credits at any time without losing track of your current usage cycle.

## How are AI credits updated?

### **1. Topping Up Credits**

When you buy additional credits, they are simply added to your existing balance.

**Example**

* Previous credits: **1500**

* Top-up: **1000**

* **New total credits: 2500**

No other values change.

### **2. Monthly Renewal**

Every plan includes a monthly free credit allowance. At renewal, we adjust usage and credits based on how much you consumed in the previous month.

**Case A: No usage**

Usage: **0** → Your total credits do **not** change.

**Case B: Usage is less than your monthly free credits**

* Previous credits: **1500**

* Usage: **200**

* Monthly free credits: **300**

→ No deduction is applied.  
→ Total credits stay **1500**.  
→ Usage resets to **0**.

**Case C: Usage exceeds your monthly free credits**

* Previous credits: **1500**

* Usage: **600**

* Monthly free credits: **500**

Overage = **600 − 500 = 100**

→ Deduct overage from total credits.  
→ New total credits: **1400**  
→ Usage resets to **0**.

### **3. Changing Your Plan**

When you switch plans, your monthly free credits may increase or decrease.

**Example**

* Startup plan: **300** free credits

* Business plan: **500** free credits

* Enterprise plan: **800** free credits

If you switch from Startups to Business, your total credits would increase by 200. Similarly, if you downgrade from Business to Startups, your total credits would decrease by 200.

Your usage remains unchanged.

## Credit Failure (Insufficient Credit Handling)

A credit failure occurs when an AI action is triggered but there are not enough credits to perform it.

**What Happens During Credit Failure**

* The action is not executed. Any available fallbacks are executed — for example, if the assistant cannot respond, the conversation is transferred directly to an agent.

* We log the failed action internally for audit
