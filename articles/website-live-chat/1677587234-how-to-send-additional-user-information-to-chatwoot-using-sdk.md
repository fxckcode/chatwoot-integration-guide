# How to send additional user information to Chatwoot using SDK?

The Chatwoot website SDK enables you to send additional user information to Chatwoot.

If you have installed our code on your website, the SDK would expose `window.$chatwoot` object. To make sure that the SDK has been loaded completely, please make sure that you listen to `chatwoot:ready` event as follows:

```
window.addEventListener("chatwoot:ready", function () {
  // Use window.$chatwoot here
  // ...
});
```

If you would like to listen to the messages in the widget you can use the following event.

```
window.addEventListener('chatwoot:on-message', function(e) {
  console.log('chatwoot:on-message', e.detail)
})
```

### SDK settings[​](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/setup#sdk-settings "Direct link to heading")

To hide the bubble, you can use the setting mentioned below.

**Note**: If you use this, you must also trigger the widget.

```
window.chatwootSettings = {
  hideMessageBubble: false,
  showUnreadMessagesDialog: false, // Disable the unread message dialog
  position: "left", // This can be left or right
  locale: "en", // Language to be set
  useBrowserLanguage: false, // Set widget language from user's browser
  type: "standard", // [standard, expanded_bubble]
  darkMode: "auto", // [light, auto]
  // baseDomain: "yourdomain.com" // configure if you want to track users across subdomains
};
```

### Use browser language in your live chat widget automatically

To show the live chat widget in the user's browser locale, set the `useBrowserLanguage` to `true` in the `window.chatwootSettings` mentioned above.

**Note**: If `useBrowserLanguage` is set to `true`, The `locale` mentioned will be ignored. If the browser language is not supported by chatwoot, the locale mentioned under `locale` will be used. If that's also missing, the widget will fall back to the `locale` of the agent dashboard.

### Dark Mode[​](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/setup#dark-mode "Direct link to heading")

Chatwoot live-chat widget supports dark mode v2.4.0 onwards. To enable the dark mode, follow the steps mentioned [here](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/live-chat-dark-mode).

### Widget designs[​](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/setup#widget-designs "Direct link to heading")

Chatwoot supports two designs for the widget.

1. Standard (default)

   ![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBeEpVVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--cd7e6b995894f8afbcc4a48f8e159ae4e3a1a04b/standard-bubble-chatwoot-live-chatwoot.gif)

2. Expanded bubble

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBeE5VVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--2b40967d868bb213b2d4e541ca3ed0e82c7222d0/expanded-bubble-chatwoot-live-chatwoot.gif)

If you are using expanded bubble, you can customize the text used in the bubble by setting `launcherTitle` parameter on chatwootSettings as described below.

```
window.chatwootSettings = {
  type: "expanded_bubble",
  launcherTitle: "Chat with us",
};
```

### Enable popout window[​](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/setup#enable-popout-window "Direct link to heading")

In order to enable the popout window, add the following configuration to `chatwootSettings`. This option is disabled by default.

```
window.chatwootSettings = {
  // ...Other Config
  showPopoutButton: true,
}

You can also popout the chat window programatically with the `popoutChatWindow()` method.
```

### Custom messages[​](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/setup#enable-popout-window "Direct link to heading")

Customize the welcome and availability messages shown in the widget header and team status indicators.

```
window.chatwootSettings = {
  // ...Other Config

  welcomeTitle: "Need help?", // Custom widget header
  welcomeDescription: "We’re here to support you.", // Header subtitle
  availableMessage: "We’re online and ready to chat!", // When team is online
  unavailableMessage: "We’re currently offline." // When team is unavailable
};
```

### Feature toggles

Enable or disable optional UI features inside the widget:

```
window.chatwootSettings = {
  // ...Other Config

  enableFileUpload: true, // Show file attachment button
  enableEmojiPicker: true, // Enable emoji picker in the chat input
  enableEndConversation: true // Let users end the conversation
};
```

### Programatically open the popout window[​](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/setup#programatically-open-the-popout-window "Direct link to heading")

You can open the popout window programatically with the `popoutChatWindow()` method.

To initiate this, call the method like below.

```
window.$chatwoot.popoutChatWindow();
```

### Toggle the widget bubble visibility[​](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/setup#toggle-the-widget-bubble-visibility "Direct link to heading")

If you want to hide/show the Chatwoot widget bubble, you can do so with `toggleBubbleVisibility('show/hide')`

Example

```
window.$chatwoot.toggleBubbleVisibility("show"); // to display the bubble
window.$chatwoot.toggleBubbleVisibility("hide"); // to hide the bubble
```

### Trigger widget programmatically

If you want to open the chat window by clicking a link on the website, follow the method below. In your action, call the Chatwoot SDK as described below.

```
window.$chatwoot.toggle();

// Toggle widget by passing state
window.$chatwoot.toggle("open"); // To open widget
window.$chatwoot.toggle("close"); // To close widget
```

### Set the user in the widget[​](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/setup#set-the-user-in-the-widget "Direct link to heading")

```
window.$chatwoot.setUser("<unique-identifier-key-of-the-user>", {
  email: "<email-address-of-the-user@your-domain.com>",
  name: "<name-of-the-user>",
  avatar_url: "<avatar-url-of-the-user>",
  phone_number: "<phone-number-of-the-user>",
});
```

`setUser` accepts an identifier which can be a `user_id` in your database or any unique parameter which represents a user. You can pass email, name, avatar_url, phone_number as params. Support for additional parameters is in progress.

Ensure you reset the session when the user logs out of your app.

### Identity validation using HMAC[​](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/setup#identity-validation-using-hmac "Direct link to heading")

To disallow impersonation and to keep the conversation with your customers private, we recommend setting up the identity validation in Chatwoot. Identity validation is enabled by generating an HMAC(hash based message authentication code) based on the `identifier` attribute, using SHA256. Along with the `identifier` you can pass `identifier_hash` also as shown below to make sure that the user is correct one.

```
window.$chatwoot.setUser(`<unique-identifier-key-of-the-user>`, {
  name: "", // Name of the user
  avatar_url: "", // Avatar URL
  email: "", // Email of the user
  identifier_hash: "", // Identifier Hash generated based on the webwidget hmac_token
  phone_number: "", // Phone Number of the user
  description: "", // description about the user
  country_code: "", // Two letter country code
  city: "", // City of the user
  company_name: "", // company name
  social_profiles: {
    twitter: "", // Twitter user name
    linkedin: "", // LinkedIn user name
    facebook: "", // Facebook user name
    github: "", // Github user name
  },
});
```

To generate HMAC, read [identity validation](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/identity-validation). Note that implementing HMAC authentication will allow chat history to persist across sessions.

### Set custom attributes[​](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/setup#set-custom-attributes "Direct link to heading")

To set additional information about the customer, you can use customer custom attributes field. Read more about custom attributes [here](https://app.chatwoot.com/hc/chatwoot-user-guide-cloud-version/en/features-explained/470).

To set a custom attribute, call `setCustomAttributes` as follows

```
window.$chatwoot.setCustomAttributes({
  accountId: 1,
  pricingPlan: "paid",

  // Here the key which is already defined in custom attribute
  // Value should be based on type (Currently support Number, Date, String and Number)
});
```

You can view these information in the sidepanel of a conversation.

To delete a custom attribute, use `deleteCustomAttribute` as follows

```
window.$chatwoot.deleteCustomAttribute("attribute-key");
```

### Set language manually[​](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/setup#set-language-manually "Direct link to heading")

```
window.$chatwoot.setLocale("en");
```

To set the language manually, use the `setLocale` function.

### Set labels on the conversation[​](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/setup#set-labels-on-the-conversation "Direct link to heading")

Please note that the labels will be set on a conversation if the user has not started a conversation. In that case, the following items will not have any effect:

```
window.$chatwoot.setLabel("support-ticket");

window.$chatwoot.removeLabel("support-ticket");
```

### Refresh the session (use this while you logout the user from your app)[​](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/setup#refresh-the-session-use-this-while-you-logout-the-user-from-your-app "Direct link to heading")

```
window.$chatwoot.reset();
```

### Widget errors[​](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/setup#widget-errors "Direct link to heading")

To see any errors in the widget, please make sure that you listen to `chatwoot:event` event as follows:

```
window.addEventListener("chatwoot:error", function () {
  // ...
});
```

Note: This feature is available in v2.3.0 and later.

### Customize the welcome header, description

You can change:

* The welcome title and description

* Messages shown when your team is online or offline

* Selectively enable UI features like file upload, emoji picker, and end conversation button

```
window.chatwootSettings = {
  welcomeTitle: 'Need help?',
  welcomeDescription: 'We’re here to support you.',
  availableMessage: 'We’re online and ready to chat!',
  unavailableMessage: 'We’re currently offline.',

  enableFileUpload: true,
  enableEmojiPicker: true,
  enableEndConversation: true
 };
```
