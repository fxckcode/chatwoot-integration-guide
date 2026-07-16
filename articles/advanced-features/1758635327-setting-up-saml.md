# Setting up SAML Authentication

This is a guide on setting up SAML auth for your account, the guide assumes you have a work IdP in place.

Before you get started, there are some points to take note of

* Once SAML is enabled, your users won't be able to access Chatwoot with their password. Disabling SAML will revert this behaviour.

* If a user is part of multiple accounts, and any one account has SAML setup, they will have to login via SAML IdP only. It's best to restrict users to your domain alone.

## Setting up SAML

You can find the SAML settings under Settings > Security. Here are the settings you need to be aware about.

* **SSO URL:** The specific HTTPS address on the Identity Provider where a SAML login begins; your app redirects users here to authenticate. Think of it as the IdP’s “login endpoint” that accepts SAML AuthnRequests and starts the SSO flow.

* **Identity Provider Entity ID:** A globally unique identifier (usually a URI-looking string) that names the Identity Provider in SAML metadata. Your Service Provider uses it to pick the right IdP config and to validate that inbound SAML messages really claim to be from that IdP.

* **Signing Certificate:** The IdP’s X.509 public certificate used to sign SAML responses/assertions. Your Service Provider stores this cert and verifies signatures with it, ensuring the message wasn’t altered and truly came from the IdP.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSHdGVlFJPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--4aeda8a3edb4e96e36bf70a0d1745c120824e7b0/image.png)Once setup, you will find the details required to register Chatwoot as a Service Provider (SP) on your SAML provider. Here are the details you will get

* **ACS URL:** The Assertion Consumer Service endpoint on the Service Provider that receives the SAML Response from the IdP. After the user authenticates, the IdP posts the signed assertion to this HTTPS URL, where your app validates it and creates a session.

* **SP Entity ID:** The unique identifier (often a URI) for the Service Provider in SAML metadata. The IdP uses this value to ensure it’s issuing a response for the correct application and to select the right ACS URL and settings.

> In case, you need this information before-hand, here's the format for it
>
> * ACS URL: `<your-chatwoot-installation>/omniauth/saml/callback?account_id=<your-account-id>`
>
> * SP Entity ID: `<your-chatwoot-installation>/saml/sp/<your-account-id>`

## Mapping Data

The following attribute mappings must be configured in your identity provider

* `email`

* `first_name`

* `last_name`

Once the user logs in for the first time, this information is used to create a user for them. It does not update the information

## Authenticating

You can navigate to this link `https://app.chatwoot.com/app/login/sso` to view the SAML login form. Just enter the email address and the app will redirect you to the configured SAML provider.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCR2tkVlFJPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--ec2bfa6daaf423fa1fed8ef63f7ac0974becaaf7/image.png)
