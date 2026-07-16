# How to translate messages with Google Translate?

If you frequently receive queries in languages you/your team members don't understand, you can utilize the Google Translate integration in Chatwoot. When enabled, you can instantly translate incoming messages using the right-click menu. This way, you can easily communicate with customers in their native language, even if you don't speak it yourself.

## How to enable Google Translate in Chatwoot?

**Step 1.** Go to Settings -> Applications -> Google Translate. Click the corresponding "Configure" button.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBOWtkVWc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--12948f0cf820cc10beab8b06989934f8cd9d71e9/google%20translate%20integration%20in%20chatwoot.png)

**Step 2.** You'll see the Google Translate app page. Click the "Connect" button.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBOXdkVWc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--e00f04387bbe6d9471ad840da6ba6e8fdf58a543/connect%20google%20translate.png)

**Step 3.** Enter your Google Cloud Project ID and Project Key File. If you need help obtaining these values, refer to this [doc](https://cloud.google.com/translate/docs/setup) from Google.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBK1VkVWc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--2526db2e7aef7a73a525dee0ac51d92ba6f150da/google%20translate%20setup.png)

Once you have entered the values, click the "Create" button.

Now, your Google Translate integration is complete.

### How to change the translation language?

Your messages get translated into your site language. To select your site language, visit the "Account Settings" page.

**Step 1.** Go to Settings -> Account Settings -> Site Language. Open the dropdown and select your preferred language.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBK2NkVWc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--aca97f8eed645c6e750db45acd044ff8f0829154/site%20language%20setting%20in%20chatwoot.png)

**Step 2.** Click the "Update Settings" button on the top-right corner of the page. This will translate your entire dashboard to the selected language.

**Note:** Agents can select their individual preferred languages too.

## How to translate incoming messages?

Whenever you receive a message in a language you need help with, click the 3 dots beside the message to open the menu and select "Translate".

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBK3dkVWc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--24951e09929b36da5bb3a43d5d3cd39ce702b71e/translating%20a%20message%20in%20chatwoot.png)

Find the translated content inline.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRFI1THdFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--c195850635f9d69c85ee2d93d030bf338b879172/translation.png)

## How to create a service account in Google Cloud Console?

To create a service account for the Google Translate API, start by signing in to the [Google Cloud Console](https://console.cloud.google.com/) and selecting or creating a new project. Once your project is ready, enable the **Cloud Translation API** by navigating to **“APIs & Services” > “Library”** and searching for “Cloud Translation API.” Click “Enable” to activate it for your project. Enabling billing is also necessary if you haven’t done so already.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCS1o1THdFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--f0370bb16aeacb9baae627e092051e1314ca9187/translation-api.png)

Next, go to **“IAM & Admin” > “Service Accounts”** and click **“Create Service Account.”**  Provide a name (e.g., translate-api-user) and continue to assign the **“Cloud Translation API User”** role. 

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSHQ1THdFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--81ff34afae408abd43415a8a8cbab0525a9bb1ea/create%20service%20account.png)

After creating the service account, navigate to the **“Keys”** section, click **“Add Key,”** and select **“Create New Key”** in **JSON** format. Download and securely store this JSON file.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSWQ1THdFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--4565f8b63ff74daaa773df9b0cf2d1cca048344c/createprivatekey.png)

Use the contents of the file you received above in the **Google Cloud Project Key file** input field in Chatwoot.
