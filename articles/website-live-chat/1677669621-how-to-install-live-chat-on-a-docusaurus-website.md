# How to install live chat on a Docusaurus website?

Chatwoot integrates seamlessly with Docusaurus via the `@chatwoot/docusaurus-plugin`. This plugin helps you easily install the Chatwoot live-chat widget on a Docusaurus-powered website.

To install the plugin, follow the quick steps explained below.

**Step 1.** Add the plugin to your project.

```
yarn add @chatwoot/docusaurus-plugin
```

or

```
npm install @chatwoot/docusaurus-plugin --save
```

**Step 2.** Configure the plugin in `docusaurus.config.js`

```
// docusaurus.config.js
module.exports = {
  plugins: ["@chatwoot/docusaurus-plugin"],
  themeConfig: {
    chatwoot: {
      websiteToken: "Your website inbox token",
      baseURL: "https://app.chatwoot.com",  // optional
      enableInDevelopment: false,  // optional
      chatwootSettings: {
        hideMessageBubble: false,
        position: "left", // This can be left or right
        locale: "en", // Language to be set
        useBrowserLanguage: false, // Set widget language from user's browser
        darkMode: "auto", // [light, auto]
        type: "expanded_bubble",
        launcherTitle: "Chat with us",
      }
    }
  }
};
```
