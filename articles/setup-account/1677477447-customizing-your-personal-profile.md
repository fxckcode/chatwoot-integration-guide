# Customizing your personal profile

Your **Profile Settings** page is where you personalize Chatwoot for yourself — your name and avatar, the dashboard's appearance, how you send messages, your signature, your password, your alerts, and your API access token. Everything here applies to *you* only; nothing on this page changes the experience for your teammates.

Click your avatar in the bottom-left corner of the dashboard and choose **Profile settings**.

---

### Profile picture

Upload a photo by clicking **Upload image**. After uploading you'll see options to **Update image** (replace it) or **Remove**. Once it's saved, you'll see a *"Avatar has been deleted successfully"* alert if you remove it, or a confirmation alert if you upload a new one.

*Use a clear, recognizable headshot. This is the avatar customers see on your replies.*

### Your full name

Your real name. Used on emails and in some internal references.

### Display name

The name shown to customers in conversations. Many agents use just a first name here ("Sarah") even when their full name is something more formal ("Sarah Anne Whitman"). If you leave it blank, your full name is used.

### Your email address

The address you log in with. Important: **changing your email forces you to log in again** — Chatwoot logs you out so you can re-authenticate with the new credentials. You'll see *"Your profile has been updated successfully, please login again as your login credentials are changed"* when this happens.

*On some installations the email field is locked (when admins disable user profile updates). If you can't edit it, that's why.*

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRTZrSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--41b98a078d0b1f33ceefa1921bbf1bbc8df3ef38/profile-image.jpg)

When you've made your changes, click **Update Profile** to save.

---

## Interface — appearance preferences

### Font size

Pick the size that's comfortable for your screen and eyes. Changes take effect immediately.

### Preferred Language

The language Chatwoot's UI uses for *you*. The default is **Use account default** — meaning whatever your administrator set under Account Settings. Pick a specific language to override that for your own session. This doesn't change anything customer-facing; it's purely for the dashboard you see.

\
![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSnFrSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--7ddd57c416be521bed2544cde7e277c536d6bd08/interface.jpg)

---

## Set your personal message signature[**​**](https://www.chatwoot.com/docs/user-guide/setup-your-account/configure-your-profile#set-your-personal-message-signature "Direct link to heading")

A signature block that's automatically appended to every reply you send from any inbox. Useful for sign-offs, support hours, or links to documentation.

The editor supports rich formatting and inline images. Inline images are supported in live-chat, email, and API inboxes; in some other channel types the image will be skipped.

Type or paste your signature, then click **Save message signature**. You'll see *"Signature saved successfully"* on success.

\
![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQ2lsSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--638b23a25921b6a362c93b2e1cd15e2e486414a5/personal-message-signature.jpg)

A typical signature:

```

---
Sarah
Acme Customer Success
sarah[@]acme.com · acme.com/help
```

---

## Hotkey to send messages

Choose how you send a reply. Two options, picked by clicking the card you prefer:

* **Enter (↵)** — pressing Enter sends the message; Shift+Enter inserts a new line

* **Cmd/Ctrl + Enter (⌘ + ↵)** — pressing Enter inserts a new line; Cmd/Ctrl+Enter sends the message

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRVNtSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--ddfdf677e13e1b3323c188b8942f0c6d630cab0f/hotkey.jpg)

---

## Reset your password[​](https://www.chatwoot.com/docs/user-guide/setup-your-account/configure-your-profile#change-your-password "Direct link to heading")

A single **Change password** button. Click it to expand a form with three fields:

- **Current password** — your existing password

- **New password** — must be at least 6 characters

- **Confirm new password** — must match the new password

This section is hidden on installations that disable user profile updates (typically when SAML SSO handles authentication centrally). Updating your password signs you out of all your other devices. Be ready to log back in everywhere you use Chatwoot.

As a security measure, you need to provide your existing password to change it to a new one. If you have forgotten the old password, you can log out of the system and reset the password. Password must contain at least one uppercase character (A-Z), at least one numeric character (0..9), and at least one special character (!@#$%^&*()_+-=[]{}|'"/^.,<>:;?~).

\
![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCT3FtSVFVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--8b1d85764dfbd3ac4c9f264f4f3f96d766654db8/change-password.jpg)

Next: [Setting up notifications](https://chatwoot.help/hc/user-guide/articles/1731478912-setting-up-notifications)
