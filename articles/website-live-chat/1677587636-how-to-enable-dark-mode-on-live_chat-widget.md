# How to enable dark mode on live-chat widget?

Modern websites enable users to switch between light and dark modes. Therefore, a live chat that works with both themes is important. This guide helps you set up dark mode for the Chatwoot live-chat widget on your website.

Here is a quick glimpse of how dark mode functions on the live chat widget:

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBMWxWVHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--5d153c8a5f8b37f33f0dfaabb226c178f7ebb4b8/dark-mode-widget-chatwoot.gif)

To enable dark mode on Chatwoot widget, use the `darkMode` parameter along with the [chatwootSettings](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/setup).

`darkMode` parameter supports two values.

1. `light` - Enable only light mode. This is the default value.

2. `auto` - Enable dark mode based on the operating system preference.

```
window.chatwootSettings = {
  //... other Settings
  darkMode: "auto",
};
```

Note: `dark` only is not supported now. We will add the support in future releases.
