# Understanding Contact Identity and Identity Validation in Chatwoot

When a customer contacts your team, Chatwoot creates or updates a contact profile for them. This profile helps agents understand who the customer is, what conversations they had before, and which channel they used.

For example, the same customer may contact you through:

* Website live chat

* WhatsApp

* Email

* An in-app support widget

Chatwoot can use identifiers such as an email address, phone number, or unique customer ID to connect these interactions to the same customer profile.

## Contact matching vs identity validation

There are two related but different ideas:

**Contact matching** helps Chatwoot recognize that two conversations may belong to the same customer.

**Identity validation** helps Chatwoot confirm that the customer is really allowed to use that identity.

This distinction matters because someone could type another customer’s email address into a public chat form. Contact matching alone can store the email, but it does not prove that the visitor owns that email or account.

## What agents see when identity is not verified

When a customer identity is not verified, Chatwoot shows a warning indicator near the contact name. This helps agents understand that the visitor has not been securely verified by your application.

\
![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSFplcXdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--17ebdde849f97f32f6363388692e83cc2d79c922/CleanShot%202026-06-24%20at%2010.47.46@2x.png)

This does not always mean the customer is suspicious. It simply means Chatwoot has not received a trusted identity validation token for that visitor.

For sensitive requests, agents should be careful before discussing private information such as billing, account details, transactions, or verification status.

### Why identity validation matters

Identity validation helps protect private customer conversations. It reduces the risk of impersonation, especially when support happens inside a logged-in customer portal, banking app, trading platform, SaaS dashboard, or any account-based product.

For example, if a logged-in customer starts a chat from your portal, your system can securely tell Chatwoot: “This visitor is customer 12345, and we have verified that from our side.”

Chatwoot can then trust the identity because it was verified by your backend system, not just typed into a chat form.

### Recommended setup

**For public website visitors, you can use normal contact fields like name, email, and phone number.**

For logged-in users, we recommend enabling identity validation. This is useful when agents may discuss sensitive information such as:

* account details

* billing information

* orders or transactions

* KYC or verification status

* internal employee requests

* regulated customer support issues

## Where to enable identity validation

Identity validation can be configured from your website inbox settings.

Go to:               Settings -> Inboxes -> Select website inbox -> Configuration -> Identity Validation

In this section, Chatwoot shows the secret key used to generate secure identity tokens. You can also choose whether identity validation should be required for all conversations.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQUJlcXdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--fc6b46eeb4b875d28fb916147e44e12500fa530e/CleanShot%202026-06-24%20at%2010.40.38@2x.png)

\
If **Require identity validation for all conversations** is enabled, visitors must provide a valid identity token before they can start conversations. Requests without valid tokens will be rejected.

## How it works in simple terms

Your application creates a secure signature for the logged-in user. Chatwoot checks that signature before trusting the user identity.

The secret used to create this signature stays on your server. It should not be exposed in the browser.

If the signature is valid, Chatwoot treats the customer identity as verified. If identity validation is enforced and the signature is missing or invalid, Chatwoot rejects the request.

### What agents should know

Agents do not need to understand the technical setup. The important point is:

If identity validation is enabled, the customer identity shown in Chatwoot is coming from the customer’s logged-in session, not from a value they manually typed into chat.

This gives support teams more confidence when handling sensitive conversations.

### When to use identity validation

Use identity validation when the chat widget is shown inside a logged-in product or customer portal.

Examples:

* fintech client portal

* banking dashboard

* ecommerce account area

* SaaS application

* employee help desk portal

* healthcare or insurance portal

For a public marketing website, identity validation may be optional. For logged-in customer support, it is strongly recommended.

### For developers

This article explains the concept at a high level. If you are ready to configure identity validation, use this [technical setup guide](https://www.chatwoot.com/hc/user-guide/articles/1677587479-how-to-enable-identity-validation-in-chatwoot).

##
