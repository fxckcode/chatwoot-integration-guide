# How to install live chat on a Gatsby website?

If you have a website created on Gatsby, you can add a Chatwoot live chat widget and talk to your visitors in real time. This can be done in 3 simple steps using Chatwoot’s Gatsby plugin.

## Step 1. Add the Gatsby plugin to your project[​](https://www.chatwoot.com/docs/product/channels/live-chat/integrations/gatsby#1-add-the-gatsby-plugin-to-your-project "Direct link to heading")

Add `gatsby-plugin-chatwoot` to your Gatsby project.

```
npm install --save gatsby-plugin-chatwoot
```

If you are using yarn, use the following:

```
yarn add gatsby-plugin-chatwoot
```

## Step 2. Add the plugin to your Gatsby config file[**​**](https://www.chatwoot.com/docs/product/channels/live-chat/integrations/gatsby#2-add-the-plguin-to-your-gatsby-config-file "Direct link to heading")

```
// In your gatsby-config.js
plugins: [
  {
    resolve: `gatsby-plugin-chatwoot`,
    options: {
      baseUrl: "BASE_URL", // Required
      websiteToken: "WEBSITE_TOKEN", // Required
      includeInDevelopment: false, // Optional
      chatwootSettings: {}, // Optional
    },
  },
];
```

You can get your Website token and base URL from your Inbox settings in your Chatwoot account.

If you need to create a new website channel, follow the procedure illustrated [here](https://app.chatwoot.com/hc/chatwoot-user-guide-cloud-version/en/website-live-chat/474).

## Step 3. Start your server[**​**](https://www.chatwoot.com/docs/product/channels/live-chat/integrations/gatsby#3-start-your-server "Direct link to heading")

You would be able to see the Chatwoot widget on the page now.
