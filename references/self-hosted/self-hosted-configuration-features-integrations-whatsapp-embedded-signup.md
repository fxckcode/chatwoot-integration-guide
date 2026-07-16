WhatsApp Embedded Signup enables users to connect their WhatsApp Business accounts through Meta’s streamlined OAuth flow without manual webhook configuration. This significantly improves the user experience by automating the entire setup process.

## Prerequisites

1. A valid Facebook account
2. A WhatsApp Business account (or ability to create one)
3. Admin access to your Chatwoot installation

## Super Admin Configuration

Before users can use WhatsApp Embedded Signup, administrators must configure the following environment variables via the Super Admin panel at `/super_admin/app_config?config=whatsapp_embedded`:

- **WHATSAPP\_APP\_ID**: The Facebook App ID for WhatsApp Business API integration
- **WHATSAPP\_CONFIGURATION\_ID**: The Configuration ID for WhatsApp Embedded Signup flow (obtained from Meta Developer Portal)
- **WHATSAPP\_APP\_SECRET**: The App Secret for WhatsApp Embedded Signup flow (required for token exchange)

These settings must be configured by a Super Admin before the WhatsApp Embedded Signup option becomes available to users.

### Retrieving Configuration Values from Meta Developer Portal

To obtain the required configuration values:

#### 1\. Create or Access Your Facebook App

1. Go to [Meta for Developers](https://developers.facebook.com/)
2. Click on “My Apps” in the top navigation
3. Either select an existing app or click “Create App”
4. If creating a new app:
	- Choose “Business” as the app type
		- Select “Business” for “I want to connect my app to”
		- Provide app details (name, email, business portfolio)

#### 2\. Configure WhatsApp Product

1. In your app dashboard, click “Add Product”
2. Find “WhatsApp” and click “Set Up”
3. Accept the WhatsApp Business Terms

#### 3\. Retrieve App ID and App Secret

- **App ID**: Found at the top of your app dashboard or in Settings → Basic
- **App Secret**: Located in Settings → Basic (click “Show” and authenticate to reveal)

#### 4\. Obtain Configuration ID

1. Navigate to Facebook Login for Business → Configuration in the left sidebar
2. Click “Configurations”
3. Set up the configuration:
	- Select login variation to: WhatsApp Embedded Signup.
		- Select WhatsApp Account as an assets. (Give manage account permission)
		- Add required permissions. Mentioned below
4. Save the configuration
5. Copy the generated **Configuration ID**

**Important:** Before overriding the current callback URI, your app must be subscribed to receive messages for the WhatsApp Business Account. This prevents error (#100) during webhook configuration. Ensure the messages webhook field is subscribed in your app’s webhook settings.

#### 5\. Required Permissions

Ensure your app has the following permissions enabled:

- `whatsapp_business_management` - Manage WhatsApp business assets
- `whatsapp_business_messaging` - Send and receive WhatsApp messages
- `business_management` - Manage business assets

For production use, your app may need to go through App Review to get advanced access to certain features. The embedded signup flow works with Standard Access for most use cases.

## Creating a WhatsApp Channel

### Step 1: Navigate to Channel Selection

1. Go to Settings → Inboxes in your Chatwoot dashboard
2. Click on “Add Inbox”
3. Select WhatsApp from the channel options
![whatsapp_channel_selection](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/whatsapp/whatsapp_channel_selection.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=8b7a6f8661f9af83e1c67fe23710ea76)

whatsapp\_channel\_selection

### Step 2: Choose WhatsApp Cloud

Select “WhatsApp Cloud” for the quick setup through Meta (embedded signup).

![whatsapp_provider_selection](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/whatsapp/whatsapp_provider_selection.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=8ea8bfcda59fd712b8f909f7b121010d)

whatsapp\_provider\_selection

### Step 3: Start Embedded Signup

Click on “Connect with WhatsApp Business” to begin the embedded signup flow.

![whatsapp_embedded_signup_start](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/whatsapp/whatsapp_embedded_signup_start.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=a8aefb73b9e3f1f1529e9f38bc87a57a)

whatsapp\_embedded\_signup\_start

### Step 4: Facebook Authentication

You’ll be redirected to Facebook to authenticate. You need to log in with an existing Facebook account.

![whatsapp_facebook_authentication](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/whatsapp/whatsapp_facebook_authentication.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=57276e53477d7b466122d65af322350d)

whatsapp\_facebook\_authentication

### Step 5: Fill Business Information

Select an existing business portfolio or create a new one to add your phone number. Fill in the required business information:

- Business portfolio
- Business name
- Business website or profile page
- Country
- Address (optional)
![whatsapp_business_information](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/whatsapp/whatsapp_business_information.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=c0c034aa34ae4e0353b566fea26e1556)

whatsapp\_business\_information

### Step 6: Select WhatsApp Business Account

Choose an existing WhatsApp Business account or create a new one. You can also select or create a WhatsApp Business Profile.

![whatsapp_account_selection](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/whatsapp/whatsapp_account_selection.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=f2da7d66aef0bcbbe61addabb44d6b54)

whatsapp\_account\_selection

### Step 7: Complete Setup

Once you’ve completed all steps, you’ll see the success screen. Your WhatsApp Business account is now connected and ready to receive messages.

![whatsapp_setup_complete](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/whatsapp/whatsapp_setup_complete.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=ed166baf1209e0afc13b310d1d02e60e)

whatsapp\_setup\_complete

![whatsapp_app_config](https://mintcdn.com/chatwoot-447c5a93/B9wOdsckmqTHx3J4/self-hosted/images/whatsapp/whatsapp_app_config.png?w=2500&fit=max&auto=format&n=B9wOdsckmqTHx3J4&q=85&s=ff186c9aa076c656d655afb4bf817b7b)

whatsapp\_app\_config

## Key Features

- **No manual configuration required**: The entire webhook and phone number setup is automated
- **Secure OAuth based authentication**: Uses Meta’s official OAuth 2.0 flow
- **Automatic webhook and phone number configuration**: Webhooks are registered automatically
- **Real-time progress tracking**: Visual feedback during the signup process
- **Comprehensive error handling**: Clear error messages and guidance

## Commerce Policy Compliance

Meta will review your business to ensure it complies with WhatsApp’s Commerce Policy and will reach out within 24 hours if there’s an issue.

## Reference Documentation

For more technical details about WhatsApp Embedded Signup, refer to the official Meta documentation:

- [WhatsApp Embedded Signup - Meta for Developers](https://developers.facebook.com/docs/whatsapp/embedded-signup/)

## Troubleshooting

### Common Issues

1. **“WhatsApp Embedded Signup not available”**
	- Ensure your Super Admin has configured the required environment variables
		- Check that all three values (App ID, Configuration ID, and App Secret) are properly set
2. **Authentication Errors**
	- Make sure you’re using an existing Facebook account
		- Verify you have the necessary permissions for the business
3. **Business Verification Issues**
	- Ensure your business information is accurate and complete
		- Check that your business complies with WhatsApp’s Commerce Policy

### Getting Help

If you encounter issues during setup:

1. Check the Chatwoot logs for any error messages
2. Verify all environment variables are correctly configured
3. Ensure your Facebook/WhatsApp accounts meet the prerequisites
4. Contact Chatwoot support with specific error messages if the issue persists