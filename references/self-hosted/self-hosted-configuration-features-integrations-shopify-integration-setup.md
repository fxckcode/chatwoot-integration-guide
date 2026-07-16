Setting up Chatwoot Shopify integration involves 5 steps.

1. Create a Shopify app in the [shopify partner dashboard](https://partners.shopify.com/).
2. Add necessary details and save the app.
3. Configure Chatwoot with the `Client ID` and `Client secret` obtained from the Shopify app.
4. Open Chatwoot UI, navigate to integrations, select Shopify, and click connect.
5. Voila! You should now be able to use Shopify in your Chatwoot account.

## Register and configure the Shopify app

To use Shopify Integration, you need to create a Shopify app in the [shopify partner dashboard](https://partners.shopify.com/). You can find more details about creating Shopify apps at the [Shopify developer portal](https://shopify.dev/docs/apps/build).

1. Create a Shopify app.
![shopify_app_create](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/shopify/create-app.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=3a6a3353cdd251319370e3342c7fc425)

shopify\_app\_create

2. Obtain the `Client ID` and `Client Secret` for the app and configure it in your app config via `{Chatwoot installation url}/super_admin/app_config?config=shopify`
![shopify_app_domain](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/shopify/configure-app.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=638a0cb820acc7fcb4a2d3a91775afef)

shopify\_app\_domain

3. Configure the redirect URL as `{Chatwoot installation url}/shopify/callback` in app configuration.
![shopify_app_redirect](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/shopify/callback.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=deaf9df4bd4a24e846707a2bf7318cb6)

shopify\_app\_redirect

Shopify will only show up in the integrations section once you have configured these values.

## Connect Chatwoot with your Shopify account

Follow this [guide](https://chatwoot.help/hc/user-guide/articles/1742395545-how-to-track-orders-with-shopify-integration) to complete the Shopify integration.