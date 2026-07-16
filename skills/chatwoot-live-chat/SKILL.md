---
name: chatwoot-live-chat
description: Install and customize the Chatwoot live chat widget on websites — Next.js, Vue, React Native, WordPress, Webflow, Gatsby, Docusaurus, and more. Use when embedding live chat or configuring the widget SDK.
---

# Chatwoot Live Chat

Install and customize the Chatwoot live chat widget on any website or app.

## Quick Install

```html
<script>
  window.chatwootSettings = {
    hideMessageBubble: false,
    position: 'right',
    locale: 'en',
    type: 'standard'
  };
  (function(d,t) {
    var g=d.createElement(t),s=d.getElementsByTagName(t)[0];
    g.src='https://app.chatwoot.com/pwa/plugin.js';
    g.defer=1;g.async=1;s.parentNode.insertBefore(g,s);
  })(document,'script');
</script>
```

See `articles/website-live-chat/website-live-chat-settings-explained.md` for all settings.

## Platform-Specific Guides

| Platform | Article |
|----------|---------|
| Next.js | `articles/website-live-chat/how-to-install-live_chat-on-a-next-js-app.md` |
| Vue.js | `articles/website-live-chat/how-to-install-live_chat-on-a-vue-js-app.md` |
| React Native | `articles/website-live-chat/how-to-install-live_chat-on-a-react-native-app.md` |
| WordPress | `articles/website-live-chat/how-to-install-live-chat-on-a-word_press-website.md` |
| Docusaurus | `articles/website-live-chat/how-to-install-live-chat-on-a-docusaurus-website.md` |
| Gatsby | `articles/website-live-chat/how-to-install-live-chat-on-a-gatsby-website.md` |
| Webflow | `articles/website-live-chat/how-to-install-live-chat-on-a-webflow-website.md` |
| Google Tag Manager | `articles/website-live-chat/how-to-install-live-chat-using-google-tag-manager.md` |

## Advanced Features

| Feature | Article |
|---------|---------|
| Custom user data via SDK | `articles/website-live-chat/how-to-send-additional-user-information-to-chatwoot-using-sdk.md` |
| Identity validation (HMAC) | `articles/website-live-chat/how-to-enable-identity-validation-in-chatwoot.md` |
| Dark mode | `articles/website-live-chat/how-to-enable-dark-mode-on-live_chat-widget.md` |
| Continue via email | `articles/website-live-chat/how-to-continue-conversations-through-email.md` |
| Contact identity | `articles/website-live-chat/understanding-contact-identity-and-identity-validation-in-chatwoot.md` |

## Identity Validation (HMAC)

Prevent impersonation with HMAC-based validation:

```javascript
// Server-side
const crypto = require('crypto');
const hmac = crypto.createHmac('sha256', CHATWOOT_SECRET_KEY);
hmac.update(contact_identifier);
const identifierHash = hmac.digest('hex');

// Client-side
window.chatwootSettings = {
  identifier: user.email,
  identifierHash: identifierHash,
  user: { name: user.name, email: user.email, avatar_url: user.avatar }
};
```

See `articles/website-live-chat/how-to-enable-identity-validation-in-chatwoot.md`.

## Pre-Chat Forms

Customize the form customers see before starting a chat:
- Add custom fields, make required/optional
- See `articles/advanced-features/how-to-use-pre_chat-forms.md`
