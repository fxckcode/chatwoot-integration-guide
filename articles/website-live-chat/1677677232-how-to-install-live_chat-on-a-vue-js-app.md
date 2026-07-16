# How to install live-chat on a Vue.js app?

To integrate Chatwoot with your Vue.js application, you need to paste the Chatwoot widget script in your Vue.js application's `index.html` file.

Here is how to do this:

## Step 1. Get your widget script[​](https://www.chatwoot.com/docs/product/channels/live-chat/integrations/vue#1-get-your-widget-script "Direct link to heading")

Your widget script can be found in your Website Inbox settings. Go to Settings -> Inboxes -> Select your Website channel > `Configuration` tab.

If you haven't created a website inbox yet, you can find the step-by-step instructions [here](https://app.chatwoot.com/hc/chatwoot-user-guide-cloud-version/en/website-live-chat/474).

## Step 2. Copy the script[**​**](https://www.chatwoot.com/docs/product/channels/live-chat/integrations/vue#2-copy-the-script "Direct link to heading")

Copy the script that was created in the `code` field of the channel.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBK2x6VHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--742964bf7893816db8255942c6e56582a9d9bc93/script%20for%20a%20website%20inbox.png)

## Step 3. Paste the script here[​](https://www.chatwoot.com/docs/product/channels/live-chat/integrations/vue#3-paste-the-script-here "Direct link to heading")

Open your Vue project and paste the script into the index.html file, right before the closing `</body>` tag.

```
<body>
  <noscript>
    <strong
      >We're sorry but <%= htmlWebpackPlugin.options.title %> doesn't work
      properly without JavaScript enabled. Please enable it to continue.</strong
    >
  </noscript>
  <div id="app"></div>
  <!-- built files will be auto injected -->

  <!-- Chatwoot script goes here -->
  <script>
    (function (d, t) {
      var BASE_URL = "https://example.com";
      var g = d.createElement(t),
        s = d.getElementsByTagName(t)[0];
      g.src = BASE_URL + "/packs/js/sdk.js";
      g.defer = true;
      g.async = true;
      s.parentNode.insertBefore(g, s);
      g.onload = function () {
        window.chatwootSDK.run({
          websiteToken: "yZ7USzaEs7hrwUAHLGwjbxJ1",
          baseUrl: BASE_URL,
        });
      };
    })(document, "script");
  </script>
  <!-- Chatwoot script goes here -->
</body>
```

## Step 4. Check![​](https://www.chatwoot.com/docs/product/channels/live-chat/integrations/vue#4-check "Direct link to heading")

You will be able to see the Chatwoot widget on the page now. Something like this:

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBL2R6VHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--2f073ca9ea425355fb29783559691c9521a8f00b/vue.png)

### Vue.js, Nuxt.js module[​](https://www.chatwoot.com/docs/product/channels/live-chat/integrations/vue#vuejs-nuxtjs-module "Direct link to heading")

A community-maintained module (Made by the awesome folks at [@huntersofbook](https://github.com/huntersofbook/huntersofbook)) for integrating Chatwoot in your Vue 3 and Nuxt 3 projects is available. You can find a [demo here](http://vue-chatwoot-plugin.vercel.app/).

* View [Vue 3 module](https://github.com/huntersofbook/huntersofbook/tree/main/projects/chatwoot/packages/vue).

* View [Nuxt 3 module](https://github.com/huntersofbook/huntersofbook/tree/main/projects/chatwoot/packages/nuxt).
