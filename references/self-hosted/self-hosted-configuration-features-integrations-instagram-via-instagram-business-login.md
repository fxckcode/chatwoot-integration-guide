Please ensure you have installed version v4.1 or above. If not, please refer to this [guide](https://developers.chatwoot.com/self-hosted/configuration/features/integrations/instagram-channel-setup) for the Facebook Login method.

Use this guide to connect Instagram professional accounts to a self-hosted Chatwoot installation using Instagram Business Login. This is the recommended authentication method for Chatwoot Instagram inboxes from v4.1 onwards.

## Prerequisites

1. A valid Facebook account.
2. A valid Instagram professional account.

## Register a Facebook app

To use the Chatwoot Instagram channel, create a Facebook app in the developer portal. You can find more details about creating Facebook apps [here](https://developers.chatwoot.com/self-hosted/configuration/features/integrations/facebook-channel-setup).

1. Click on the “Create App” button
![facebook_create_app](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook-create-app.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=ddfd65fab93bc934c48e9c93e7628c28)

facebook\_create\_app

2. Select the option “Other”.
![facebook_other_app](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook_other_app.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=7746d5bd00665aabecbe80443ad56ac9)

facebook\_other\_app

3. For the app type, choose “Business”
![facebook_business](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook_business.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=f77bb8e7a3e15335ce52dbbe745bee70)

facebook\_business

4. Add app name and connect business account
![facebook_business_details](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/facebook/facebook_business_details.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=d61d67282b8ec76d38de9912cac896d7)

facebook\_business\_details

5. Add Instagram product from the Home page.
![instagram_product](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/instagram/instagram_product.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=a987243bb7582ff24d4238b3bea5a0fd)

instagram\_product

## Configure Instagram settings for Chatwoot

1. Copy Instagram app ID and Instagram app secret
![instagram_app_id](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/instagram/instagram_app_id.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=ab34855c5c6eab7e6adf51b995055780)

instagram\_app\_id

2. Add the Instagram app ID and Instagram app secret to your app config via `{Chatwoot installation url}/super_admin/app_config?config=instagram`
![instagram_app_config](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/instagram/instagram_app_config.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=6c6cd1292215dbe9df58321e5d110693)

instagram\_app\_config

3. Configure Webhooks

Set the callback URL to `{your_chatwoot_url}/webhooks/instagram`. The verify token should match your `INSTAGRAM_VERIFY_TOKEN`, which can be configured through `app_config`

![instagram_webhooks](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/instagram/instagram_webhook.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=21881f5a1a82c083ac01115b34f97c33)

instagram\_webhooks

Subscribe to `messages`, `messaging_seen`, and `message_reactions` events.

![instagram_webhooks_subscribe](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/instagram/instagram_webhooks_subscribe.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=0a0c94dee8187be70567af542bd1c98e)

instagram\_webhooks\_subscribe

To receive web hooks, app mode should be set to “Live”.

4. Set up Instagram business login

Set Redirect URL as `{your_chatwoot_url}/instagram/callback`

![instagram_business_login](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/instagram/instagram_business_login.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=744ee53ea96a15f1c9987da8e83f9267)

instagram\_business\_login

5. Create a new Instagram tester account

## Create an Instagram inbox in Chatwoot

Head over to Chatwoot and create an Instagram inbox. Please refer to this [guide](https://chatwoot.help/hc/user-guide/articles/1744361165-how-to-setup-an-instagram-channel-via-instagram-login) for more details on creating an Instagram inbox in Chatwoot.

## Test the Instagram integration before going live

1. Add Instagram Testers by clicking “Add People” button.
![facebook_instagram_test](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/instagram/instagram-testers-list.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=83754206a492d0371a2ad8c08508a484)

facebook\_instagram\_test

2. Make sure that you have selected the role Instagram Tester while creating a new tester.
![instagram_tester_list](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/instagram/instagram-add-tester.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=541cc071b3541772e49aff2efe5283fb)

instagram\_tester\_list

## Going into production.

Before you can start using your Facebook app in production, you will have to get it verified by Facebook. Refer to the [docs](https://developers.facebook.com/docs/messenger-platform/instagram/app-review) on getting your app verified.

## Troubleshooting & Common Errors

### Insufficient Developer Role Error

Ensure the Instagram user is added as a developer: `Meta Dashboard → App Roles → Roles → Add People → Enter Instagram ID`

### API Access Deactivated

Ensure the **Privacy Policy URL** is valid and correctly set.

### Invalid request: Request parameters are invalid: Invalid redirect\_uri

Please configure the Frontend URL. The Frontend URL does not match the authorization URL.

### Instagram Channel creation Error: Failed to exchange token

Please make sure that the tester account has been added to the Facebook app settings.

### 400: Session Invalid when connecting the Instagram channel

This might be an issue from Facebook’s side. Please try again after some time.