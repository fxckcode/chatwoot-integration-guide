# Business Hours and Auto-Responder

**Business Hours** define when your team is available. They power three things:

1. **Out-of-office message** — customers who message outside working hours see a custom message instead of nothing

2. **SLA timer behavior** — when SLAs are configured to use business hours, the clock pauses overnight and on weekends

3. **Reporting accuracy** — response-time metrics can be calculated against working time instead of wall-clock time

Business Hours are set per inbox, so a US Support inbox and an EU Support inbox can have completely different schedules.

*Permissions*: Only administrators can configure an inbox's business hours and out-of-office message.

---

## Setting up business hours on an inbox

1. Go to **Settings → Inboxes** and open the inbox you want to configure.

2. Click the **Business Hours** tab.

3. Toggle **Enable business availability for this inbox** on.

4. Pick your **timezone** — all schedule times are interpreted in this timezone.

5. For each day of the week, set:

   * **Start time** and **End time**, or

   * Mark the day as **closed all day**, or

   * Mark the day as **open all day**

6. Write your **out-of-office message** — keep it short and useful. *"Thanks for reaching out! Our team is available Monday–Friday, 9am–6pm EST. We'll get back to you first thing tomorrow."* is a solid default.

7. Save.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQ2E1SXdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--57a9b8b3b5481b15da663583f818b14ee30d85ec/business-hours.jpg)

---

## What customers see?

When a customer sends an incoming message to an inbox that's currently outside its business hours, Chatwoot automatically sends the configured out-of-office message back to them as an outgoing reply. So a customer messaging your WhatsApp inbox at midnight gets the out-of-office reply on WhatsApp.

\
![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSDI2SXdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--f9d7dae96922f8894d8537a72f8bc80b67dc9cca/out-of-office.jpg)

A few rules govern when the auto-reply fires:

* The out-of-office message is sent **once per day per conversation** — repeated messages from the same customer the same day don't generate a second auto-reply.

* If an agent has sent a public reply in the conversation within the **last 5 minutes**, the auto-reply is suppressed (so a conversation that's still being actively handled at the close of business hours isn't interrupted).

The auto-reply is informational. It doesn't block the customer from sending more, and it doesn't change the conversation status. The conversation arrives normally and agents see it whenever the inbox is back in business hours.

---

## How business hours change SLA timers?

If you've configured an SLA with **Only during business hours** turned on, the timer pauses outside working hours:

* Customer messages on Friday 6pm with an SLA of 4 hours

* Inbox is closed from 6pm Friday to 9am Monday

* Timer doesn't run over the weekend

* Effective deadline: Monday 1pm (4 working hours from 9am Monday open)

If business hours are off on the SLA (or off on the inbox), the timer runs 24/7 — Friday 6pm + 4 hours = Friday 10pm.

---

## How business hours show up in reports?

In the Reports section, most reports have a Business hours toggle. When on: Average First Response Time, Resolution Time, etc. are calculated against working time only — overnight gaps don't count.

---

## Frequently asked questions

**Can I have different business hours for different days?**

Yes — you set start/end times per day independently. Saturday at 10am-2pm while Mon-Fri runs 9-6 is a normal config.

**Can I configure business hours account-wide rather than per inbox?**

Not directly. Each inbox has its own schedule. If you have many inboxes that should share the same hours, you'll need to set them on each — but that's also a feature, since teams in different timezones often staff different inboxes.

**Does Chatwoot block messages outside business hours?**

No. The inbox is always open to receiving. Business hours just control what *we* show to the customer and how the timers behave.

**What if a holiday closes the office for a day?**

There's no built-in holiday calendar. Temporarily change that day to *closed all day* and revert later.
