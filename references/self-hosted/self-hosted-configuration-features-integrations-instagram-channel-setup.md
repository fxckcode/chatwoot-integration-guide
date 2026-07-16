We recommend Instagram Business Login as the preferred authentication method, as it provides simpler configuration and a better developer experience. Please refer to this [guide](https://developers.chatwoot.com/self-hosted/configuration/features/integrations/instagram-via-instagram-business-login) for more details. We will be stopping the support for Instagram via Facebook Login in the future from v4.1 onwards.

## Prerequisites

1. A valid facebook account.
2. A valid facebook page.
3. A valid instagram professional account.

## Register A Facebook App

To use Instagram Channel, you have to create a Facebook app in the developer portal. You can find more details about creating Facebook developer app [here](https://developers.chatwoot.com/self-hosted/configuration/features/integrations/facebook-channel-setup).

1. Click on the “Create App” button
![facebook_create_app](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook-create-app.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=ddfd65fab93bc934c48e9c93e7628c28)

facebook\_create\_app

2. Select the option “Other”.
![facebook_other_app](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook_other_app.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=7746d5bd00665aabecbe80443ad56ac9)

facebook\_other\_app

3. For the app type, choose “Business”
![facebook_business](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook_business.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=f77bb8e7a3e15335ce52dbbe745bee70)

facebook\_business

3. Enter basic details like the app name and email.
![facebook_business_details](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook_business_details.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=d61d67282b8ec76d38de9912cac896d7)

facebook\_business\_details

Once you register your Facebook App, you will have to obtain the `App Id` and `App Secret`. These values will be available in the app settings and will be required while setting up Chatwoot environment variables.

![facebook_app_id](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook_app_id.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=2f4ed36576d760116893c68695515d17)

facebook\_app\_id

## Configuring the Environment Variables in Chatwoot

Configure the following Chatwoot environment variables with the values you obtained during the Facebook app setup. The `IG_VERIFY_TOKEN` should be a unique and secure string that you provide when configuring the Instagram app.

Restart the Chatwoot server after updating the environment variables

```shellscript
IG_VERIFY_TOKEN=
FB_APP_SECRET=
FB_APP_ID=
```

## Configure the Facebook App

1. In the app settings, add your “Chatwoot installation domain” as your app domain.![facebook_app_domain](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook_app_domain.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=69349deeb681d5ee4f3925491822388c)
	facebook\_app\_domain
2. Add the “Instagram Graph API” product via the Facebook app dashboard.![instagram_product](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/instagram/instagram_product.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=a987243bb7582ff24d4238b3bea5a0fd)
	instagram\_product
3. Go to the app settings and select “Webhooks”. From there, choose Instagram and click on the “Subscribe to this object” button.![instagram_webhooks](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/instagram/instagram_webhooks.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=e24a695547a322f329c3a3df2dffdf57)
	instagram\_webhooks
4. Provide the Callback URL as `{your_Chatwoot_installation_url}/webhooks/instagram` and the Verify token as `IG_VERIFY_TOKEN` from your environment variable.![instagram_webhook_url](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/instagram/instagram_webhook_url.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=d1337f01322debf51a2800facf6db0b1)
	instagram\_webhook\_url

## Connect the facebook page with instagram account

1. Go to [Facebook pages](https://www.facebook.com/pages/?category=your_pages) and select your page and open the settings
![facebook_page_settings](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/instagram/facebook_page_settings.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=e1ffd2450ad23e91261e3a8926f28d30)

facebook\_page\_settings

2. Go to “Linked accounts” and connect your instagram professional account.
![facebook_connect_instagram](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/instagram/facebook_connect_instagram.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=dcdaa8cbf019ec4963e336e795f63523)

facebook\_connect\_instagram

3. Select the option “Business”
	![instagram_connect_facebook](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/instagram/instagram_connect_facebook.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=187a5f35548b5b7b313f78c4758b741b)
	instagram\_connect\_facebook
4. Select the instgram account category
![select_category_instagram](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/instagram/select_category_instagram.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=4430df2c0827da2def9a5ec9d8948ea1)

select\_category\_instagram

5. If everything is okay, you will see the message “Instagram connected.”
![instagram_connect_success](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/instagram/instagram_connect_success.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=fbc01ed4a1c99ed7f328b3fec977dd4a)

instagram\_connect\_success

## Create Instagram Inbox in Chatwoot

1. Head over to Chatwoot and create a Messenger inbox. Please refer to this [guide](https://www.chatwoot.com/hc/user-guide/articles/1677829420-how-to-setup-an-instagram-channel) for more details on creating a Messenger inbox in Chatwoot.

So whenever you receive any message on Instagram, it will redirect to your Facebook page.

## Testing the Instagram channel

Until the application is approved for production, Facebook wouldn’t send the new messages on your instagram to Chatwoot. To test the changes until the app is approved for production. Follow the steps

1. Create a Test app for your app.
![facebook_instagram_test](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/instagram/facebook_instagram_test.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=5aceed84b487fca282b083330b232d86)

facebook\_instagram\_test

2. Add the `Instagram Graph API` product via the Facebook app dashboard.
	![instagram_product](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/instagram/instagram_product.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=a987243bb7582ff24d4238b3bea5a0fd)
	instagram\_product
3. Go to the app settings and select “Webhooks”. From there, choose Instagram and click on the “Subscribe to this object” button.
	![instagram_webhooks](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/instagram/instagram_webhooks.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=e24a695547a322f329c3a3df2dffdf57)
	instagram\_webhooks
4. Provide the Callback URL as `{your_chatwoot_installation_url}/webhooks/instagram` and the Verify token as `IG_VERIFY_TOKEN` from your environment variable.
	![instagram_webhook_url](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/instagram/instagram_webhook_url.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=d1337f01322debf51a2800facf6db0b1)
	instagram\_webhook\_url
5. Open the test app and add extra product for the test app: Instagram Basic Display
![instagram_basic_display](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/instagram/instagram_basic_display.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=6d564533e714abbc37d2b29b9a0e18b8)

instagram\_basic\_display

6. In the app settings, add the platform “Website” and give `Site URL` as your installation URL.
![instagram_app_platform](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/instagram/instagram_app_platform.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=ff99d87575886cb9cdf172c94b8f6da7)

instagram\_app\_platform

7. Head over to the Instagram Basic Display section and create a new app.
![instagram_basic_display_settings](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/instagram/instagram_basic_display_settings.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=a09bf1f0c2386566313126db1398c122)

instagram\_basic\_display\_settings

8. Add Instagram Testers by clicking “Add or Remove Instagram Testers” button.
![instagram_testers](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/instagram/instagram_testers.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=8cab67c1cd670cc8945670fdc28dbe4b)

instagram\_testers

9. Make sure that you have selected the role `Instagram Tester` while creating a new tester.
![instagram_tester_list](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/instagram/instagram_tester_list.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=2432313914665b9a9880944a4dd9bb47)

instagram\_tester\_list

10. Click on Edit subscriptions under Webhook > Instagram and subscribe to the following,

```text
message_reactions
messages
messaging_seen
```

![instagram_subscription](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/instagram/instagram_subscription.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=6272774a2fc83a4132c305889565699e)

instagram\_subscription

You should do this step for both normal and test apps.

1. Head over to Chatwoot and create a Messenger inbox. Please refer to this [guide](https://www.chatwoot.com/hc/user-guide/articles/1677829420-how-to-setup-an-instagram-channel) for more details on creating a Messenger inbox in Chatwoot.
2. Send a message to the connected Instagram account from Instagram Testers, and it should appear in Chatwoot now

## Going into production.

Before you can start using your Facebook app in production, you will have to get it verified by Facebook. Refer to the [docs](https://developers.facebook.com/docs/messenger-platform/instagram/app-review) on getting your app verified.

Obtain advanced access to the required permissions mentioned below for your Facebook app

```text
instagram_manage_messages
instagram_basic
pages_show_list (To list the pages to be connected in chatwoot)
pages_manage_metadata (Subscribe webhooks on behalf of the page)
pages_messaging (To message on behalf of the page)
business_management (For accessing user profile picture and name of people who contacts the page)
```

If your facebook app’s version is more than 7.0 then you will need extra permission according to facebook’s updated policy. Make sure you get permission for.

```text
pages_read_engagement
```

## Developing or Testing Facebook Integration in your machine

Install [ngrok](https://ngrok.com/docs) on your machine. This will be required since Facebook Messenger APIs will only communicate via https.

```shellscript
brew cask install ngrok
```

Configure ngrok to route to your Rails server port.

```shellscript
ngrok http 3000
```

Go to the Facebook developers page and navigate into your app settings. Add `localhost` as your app domain and add a privacy policy URL in the app settings. In the Webhook > Instagram settings shown in the above image, configure the callback url with the following value.

```shellscript
{your_ngrok_url}/webhooks/instagram
```

Update verify token in your Chatwoot environment variables.

You will also have to add a Facebook page to your `Access Tokens` section in your Messenger settings page. Restart the Chatwoot local server. Then, your Chatwoot setup will be ready to receive Facebook messages.

## Test your local Setup

1. After finishing the setup above, [create a Messenger inbox](https://www.chatwoot.com/hc/user-guide/articles/1677778588-how-to-setup-a-facebook-channel) after logging in to your Chatwoot Installation.
2. Send a message to your Facebook Page from your Instagram account.
3. Wait and confirm incoming requests to `/webhooks/instagram` endpoint in your ngrok screen.
4. You can also verify your callback URL by clicking on Test for the subscribed Instagram fields. Go to webhook Instagram and click on Test with `v11.0` ![subscribe](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/instagram/subscribe.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=a16c7ccc32517d62cb25b40907ab6776)

You can have only one app connected to the Chatwoot for Instagram and Facebook combined as the Messenger platform is common. But suppose you want to have separate channels for Instagram and Facebook. In that case, you can have multiple Facebook pages inside your app that would be connected to Facebook users and Instagram users separately and then connected to the different inbox in the Chatwoot page.

## Checklist

1. Integrate the Facebook test app and Send a message from the Instagram tester to the connected account.
2. Make sure your Instagram account is a business account.
3. If the Instagram test account can receive the message and forward it to the webhook URL, then submit it for review.
4. If the Instagram test account is not able to receive the message and forward it to the webhook URL
	- Check the logs if you are receiving the message to `{your-app-url}/webhooks/Instagram`
		- If the logs are present for the above endpoint, if there are any errors, then reach out to us. We will help you out.
		- If the logs aren’t present for the above endpoint, then raise a bug for the Facebook team or follow this bug [https://developers.facebook.com/support/bugs/468852858104743/](https://developers.facebook.com/support/bugs/468852858104743/)
5. If you are not facing the above issue and can get the message, but the review isn’t passing, then reach out to the reviewer.
	- When your app gets rejected, open the rejected submission. You can see the messenger icon in the bottom right corner to support you with your rejected review.
		- You can talk to the support team and ask your questions about the submission and the reason for the rejection.
6. If your test app passed the review, it’s good to go into production.
7. If you face an issue on production that you cannot receive the messages, then reach out to us with the error logs.