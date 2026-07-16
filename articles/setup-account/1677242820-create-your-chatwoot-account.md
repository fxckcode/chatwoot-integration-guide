# Creating a Chatwoot Account

This guide walks you through creating a new Chatwoot account — whether you're using **Chatwoot Cloud** (the hosted version at [chatwoot.com](http://chatwoot.com)) or your own **self-hosted** installation.

---

## Cloud or self-hosted?

Pick the path that matches your setup.

| | **Cloud** | **Self-hosted** | 
|---|-----------|----------------| 
| Where you sign up | [chatwoot.com](https://www.chatwoot.com/) | `your-installation-url/app/auth/signup` | 
| Hosting | Managed by Chatwoot | You operate the server | 
| Updates | Automatic | You handle them | 
| Best for | Most teams that want to skip ops | Teams with strict data-residency or self-management requirements |

If you're not sure which you're using, ask your IT team — or assume Cloud unless you've been told otherwise.

---

## Signing up on Chatwoot Cloud

### Step 1 — Open the signup page

Go to [chatwoot.com](https://www.chatwoot.com/) and click **Signup** button.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTFBkSXdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--9dfdfb2163e80d85bc13d08924a9e6ae5548a3f8/main-page.png)

### Step 2 — Fill in the signup form

You'll be asked for five things:

| Field | What to enter | 
|-------|---------------| 
| **Work email** | A valid work email address — this is what you'll use to log in. E.g. *john.hopkins[@]companyname.com*. | 
| **Password** | Must include at least one uppercase letter (A–Z), at least one digit (0–9), and at least one special character |

\
![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQmplSXdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--da119c1eba9d637d743af9bff752e83520490cf6/signup-page.png)

Click **Create an account** to submit.

### Step 3 — Verify your email

Chatwoot sends an email titled *"Confirmation Instructions"* to the work email you signed up with. Open it and click **Confirm my account**. The link logs you back into the dashboard.

***Can't find the email?** Check your spam folder first, then your work email's quarantine. Some organizations have email-security policies that block external automated emails from reaching the inbox — if that's the case, ask your IT admin to release the message from quarantine or allow Chatwoot's sending domain.* 

---

## Signing up on a self-hosted installation

If your team runs its own Chatwoot, the signup flow is the same, only the URL is different. Open:

```
{your-installation-url}/app/auth/signup
```

Replace `{your-installation-url}` with whatever your team uses (e.g. `support.acme.com`).

The form fields are identical to Cloud. Email confirmation works the same way, assuming your installation is configured to send email.

> Self-hosted installations often have additional configuration steps (custom domain, SMTP, SAML SSO). Those are documented separately in the [Chatwoot self-hosted guides](https://www.chatwoot.com/docs/self-hosted).

**Next Steps:**[**​**](https://www.chatwoot.com/docs/user-guide/setup-your-account/create-an-account/#next-steps "Direct link to heading")

We recommend you follow the steps below to set up your account and get the full power of Chatwoot.

You can also go through the [Chatwoot 101 lessons](https://app.chatwoot.com/hc/chatwoot-user-guide-cloud-version/en/chatwoot-101/378) to learn the ins and outs of effective customer engagement using Chatwoot.

* [Configure your profile](https://www.chatwoot.com/hc/user-guide/en/categories/chatwoot-101): Set your name, picture, password, and more.

* [Configure account details](https://www.chatwoot.com/hc/user-guide/articles/1677480617-customizing-your-general-settings): Setup your account’s name, language, etc.

* [Add Agents](https://www.chatwoot.com/hc/user-guide/articles/1677482414-adding-agents): Add your team members to your account to help manage conversations.

* [Add Inboxes](https://app.chatwoot.com/hc/chatwoot-user-guide-cloud-version/en/setup-account/464): Add your conversation inboxes/channels like website widget, Facebook, WhatsApp, etc.

* [Configure your chat widget](https://www.chatwoot.com/hc/user-guide/en/categories/website-live-chat): Personalize your website chat widget.

* [Add Teams](https://www.chatwoot.com/hc/user-guide/articles/1677492970-adding-teams): Setup your teams like Sales, Services, Product, etc.

* [Add Labels](https://www.chatwoot.com/docs/user-guide/add-label-settings): Setup labels for categorizing your contacts/conversations.

* [Add Canned Responses](https://www.chatwoot.com/hc/user-guide/articles/1677501325-how-to-create-saved-reply-templates-with-canned-responses): Create your saved reply templates for frequently asked questions.

* [Integrations](https://www.chatwoot.com/docs/user-guide/integrations): Integrate Chatwoot with your favorite apps, or use Webhooks.

* [Applications](https://www.chatwoot.com/docs/user-guide/applications): Connect your account with applications for better workflows.
