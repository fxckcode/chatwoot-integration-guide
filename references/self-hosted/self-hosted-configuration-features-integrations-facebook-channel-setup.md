To use Facebook Channel, you have to create a Facebook app in the developer portal. You can find more details about creating Facebook apps [here](https://developers.facebook.com/docs/apps/#register).

## Prerequisites

1. A valid facebook account.
2. A valid facebook page.

## Register A Facebook App

1. Go to [Facebook developer portal](https://developers.facebook.com/apps/) and click on the “Create App” button
![facebook_create_app](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook-create-app.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=ddfd65fab93bc934c48e9c93e7628c28)

facebook\_create\_app

2. Select the option “Other”.
![facebook_other_app](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook_other_app.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=7746d5bd00665aabecbe80443ad56ac9)

facebook\_other\_app

3. For the app type, choose “Business”.
![facebook_business](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook_business.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=f77bb8e7a3e15335ce52dbbe745bee70)

facebook\_business

3. Enter basic details like the app name and email.
![facebook_business_details](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook_business_details.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=d61d67282b8ec76d38de9912cac896d7)

facebook\_business\_details

Once you register your Facebook App, you will have to obtain the `App Id` and `App Secret`. These values will be available in the app settings and will be required while setting up Chatwoot environment variables.

![facebook_app_id](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook_app_id.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=2f4ed36576d760116893c68695515d17)

facebook\_app\_id

## Configuring the Environment Variables in Chatwoot

Configure the following Chatwoot environment variables with the values you obtained during the Facebook app setup. The `FB_VERIFY_TOKEN` should be a unique and secure string that you provide when configuring the Facebook app. Generate a random string and set it as the `FB_VERIFY_TOKEN`. Facebook will include this string in all verification requests.

Restart the Chatwoot server after updating the environment variables

```shellscript
FB_VERIFY_TOKEN=
FB_APP_SECRET=
FB_APP_ID=
```

## Configure Facebook Login

1. Add the Facebook Login product via the Facebook app dashboard.
![facebook_app_login](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook_app_login.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=12f3129bf4773bc27ef615bc5dcb26ad)

facebook\_app\_login

2. Enable `Web OAuth Login`, `Login with Javascript SDK` and add your self-hosted domain to the `Allowed Domains for the JavaScript SDK` input.
![facebook_sdk_login](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook_sdk_login.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=5ef9c156947aa9038cd58246024c08ff)

facebook\_sdk\_login

## Configure the Facebook App

1. In the app settings, add your `Chatwoot installation domain` as your app domain.
![facebook_app_domain](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook_app_domain.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=69349deeb681d5ee4f3925491822388c)

facebook\_app\_domain

2. In the products section in your app settings page, Add “Messenger”
![facebook_messenger_product](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook_messenger_product.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=a42c0fdd2508fb622abada50a9367d7f)

facebook\_messenger\_product

3. Go to the Messenger settings and configure the call back URL
![Alt text](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook_messenger_section.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=7ea2936ca6609d66d7256a030a204ed1)
4. Provide the Callback URL as `{your_chatwoot_installation_url}/bot` and the Verify token as `FB_VERIFY_TOKEN` from your environment variable.
![facebook_callback_url](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook_callback_url.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=94007e24d4b8e722c76f45d21617cda3)

facebook\_callback\_url

5. Head over to Chatwoot and create a Messenger inbox. Choose a page for which your Facebook developer account has admin access to. Please refer to this [guide](https://www.chatwoot.com/hc/user-guide/articles/1677778588-how-to-setup-a-facebook-channel) for more details on creating a Messenger inbox in Chatwoot.

## Testing the Facebook channel

Until the application is approved for production, Facebook wouldn’t send the new messages on your page to Chatwoot.

To test the changes until the app is approved for production. Follow the steps

1. Head over to the messenger section in your app settings page, in Facebook developers.
![facebook_messenger_settings](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook_messenger_settings.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=dd0a6b0583c47637619abacd23514b4c)

facebook\_messenger\_settings

2. Click `Add or remove pages` and connect the page which you choose while creating the Chatwoot Messenger inbox.
![facebook_callback_pages](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook_callback_pages.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=56bc918fe5f12081846b7fa8a56d8723)

facebook\_callback\_pages

3. After connecting the pages, Click on `Add subscriptions` from the connected page.
![facebook_page_config](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook_page_config.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=b1cc3c7b30d4982ff152806822022531)

facebook\_page\_config

4. Subscribe to the following fields and save the subscription.

```text
messages
messaging_postbacks
message_deliveries
message_reads
message_echoes
```

![facebook_page_subscription](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook_page_subscription.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=7e6592a2d58462fe36cf9c955e77ddfa)

facebook\_page\_subscription

4. Send a message to the connected page from your Facebook account and it should appear in Chatwoot now.

## Going into production.

Before you can start using your Facebook app in production, you will have to get it verified by Facebook. Refer to the [docs](https://developers.facebook.com/docs/apps/review/) on getting your app verified.

Obtain advanced access to the required permissions mentioned below for your Facebook app

```text
pages_messaging (To message on behalf of the page)
pages_show_list (To list the pages to be connected in chatwoot)
pages_manage_metadata (Subscribe webhooks on behalf of the page)
business_management
pages_read_engagement (Read followers data (including name, PSID), and profile )
Business Asset User Profile Access  (For accessing user profile picture and name of people who contacts the page)
```

Make sure your facebook app subscription version is 17.0, we have updated the FB subscription with the latest version, so change the permission subscription version under the facebook app webhooks option.

## Developing or Testing Facebook Integration in your machine

Install [ngrok](https://ngrok.com/docs) on your machine. This will be required since Facebook Messenger API’s will only communicate via https.

```shellscript
brew cask install ngrok
```

Configure ngrok to route to your Rails server port.

```shellscript
ngrok http 3000
```

Go to the Facebook developers page and navigate into your app settings. In the app settings, add `localhost` as your app domain. In the Messenger settings page, configure the callback url with the following value.

```shellscript
{your_ngrok_url}/bot
```

Update verify token in your Chatwoot environment variables.

You will also have to add a Facebook page to your `Access Tokens` section in your Messenger settings page. Restart the Chatwoot local server. Your Chatwoot setup will be ready to receive Facebook messages.

## Facebook API version

We support facebook API version v13.0 going forward, which you can update in the facebook app advanced settings.

![fb_api_version](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/fb_api_version.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=d2c46f4c55cc859d2723f88b60681052)

fb\_api\_version

## Test your local Setup

1. After finishing the set-up above, [create a Facebook inbox](https://www.chatwoot.com/hc/user-guide/articles/1677778588-how-to-setup-a-facebook-channel) after logging in to your Chatwoot Installation.
2. Send a message to your page from Facebook.
3. Wait and confirm incoming requests to `/bot` endpoint in your ngrok screen.