# Common WhatsApp issues and how to fix them

## WhatsApp Messages Not Received Even Though Everything Looks Connected

### Symptoms

* WhatsApp channel is connected successfully

* Phone number status shows **Connected**

* Quality rating is **Green**

* No errors are shown in Chatwoot

* Outgoing messages may work, but **incoming messages are not received**

### Why This Happens

In some cases, Meta requires the WhatsApp phone number to be **registered again**, even though it still appears connected and healthy.

This usually happens after:

* A display name change

* Business profile updates

* Certain internal Meta-side sync issues

When this occurs, WhatsApp messages may silently stop being delivered without showing any visible errors. This is a known Meta behavior.

### How to Fix It

Re-registering the WhatsApp phone number resolves the issue immediately (Please ask us in the support and will resolve it for you)

* No plan changes are required

* No webhook changes are required

* In most cases, **no new verification code is needed**

Once the number is registered again, message delivery resumes normally.

## Display Name Status Issues (Pending / Rejected / Not Approved)

### What Is a Display Name?

The display name is the business name shown to customers on WhatsApp.\
Meta reviews and approves this name before it becomes active.

### Common Display Name Statuses

* **Approved** – Everything is good, no action needed

* **Pending** – Meta is reviewing the name

* **Rejected** – The name did not meet Meta’s guidelines

### Why Display Name Issues Matter

* A rejected or pending display name can delay onboarding

* Changing the display name may require **re-registering the phone number**

* Messages may fail or stop working if registration is not completed after approval

### Common Reasons for Rejection

* Name does not match the business name in Meta Business Manager

* Use of generic words (e.g., “Support”, “Official”, “Service”)

* Use of emojis, symbols, or all caps

* Mismatch between brand name and website/domain

### Best Practices for Display Names

* Use your **official business or brand name**

* Match the name used in your website and Meta Business Manager

* Avoid emojis, slogans, or extra descriptors

* Keep it simple and brand-consistent

### Important Note

After a display name is approved, Meta may still require the phone number to be **registered again** for the change to fully take effect.

If WhatsApp messages stop working after a display name update, re-registering the number usually fixes the issue.

## WhatsApp Error 131049 – User Has Not Accepted WhatsApp Terms of Service

### What Is Error 131049?

Error 131049 means that the recipient has not accepted WhatsApp’s latest Terms of Service.

This error is returned by WhatsApp, not Chatwoot, and is specific to the customer’s phone number, not your business setup.

### When Does This Error Occur?

You may see error 131049 when:

* Sending a message to a user who hasn’t opened WhatsApp recently

* WhatsApp has released updated Terms of Service

* The user hasn’t accepted the new terms in their WhatsApp app

In this state, WhatsApp **blocks message delivery** to that user until they accept the terms.

### Why This Happens

WhatsApp requires all users to explicitly accept updated Terms of Service before they can:

* Receive messages from businesses

* Participate in business conversations

Until the user accepts the terms, WhatsApp will reject messages with error **131049**.

### How to Fix Error 131049

This issue **cannot be fixed from Chatwoot or your WhatsApp Business account**.

The **end user must**:

1. Open their WhatsApp app

2. Accept the latest Terms of Service prompt

Once the user accepts the terms, messages will start delivering automatically—no retry or configuration change is required.
