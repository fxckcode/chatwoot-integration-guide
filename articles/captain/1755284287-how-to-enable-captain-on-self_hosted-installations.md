# How to enable Captain on self-hosted installations?

Captain is an AI assistant that helps you respond faster and more accurately. With **Bring Your Own Key (BYOK)**, you can use your own API key from OpenAI or any compatible AI service. You control the data, costs, and which model is used. In a self-hosted setup, Captain only sends data to the AI model you choose. 

This guide will show you how to enable Captain in your **self-hosted Enterprise Edition**, add your API key, and set up a custom model if you want.

## Prerequisites

Before you begin, make sure that you have:

* **Chatwoot Enterprise Edition** with a paid plan.

* Admin access to the **Super Admin Console**.

* A valid **OpenAI API key**.

* (Optional) A self-hosted **OpenAI-compatible API endpoint**.

* (Optional) A [**Firecrawl API key**](https://www.firecrawl.dev/) for a better documentation crawling.

## Enabling Captain in the Super Admin Console

To enable Captain at the installation level:

Log in to the **Super Admin Console**. Navigate to **Settings → Captain**.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTmNKL1FFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--a3ab35644fcf7dc2bd5efc131fbe219e1305ca31/Screenshot%202025-08-15%20at%2011.51.50%E2%80%AFAM.png)

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQ3NLL1FFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--8a4b8f28eaaa80f8fae85881aa9345ea1e8cb8c4/Screenshot%202025-08-15%20at%2011.50.26%E2%80%AFAM.png)

Fill in the configuration fields:

1. **OpenAI API Key** *(Required)* – The key for authenticating requests to OpenAI or a compatible service.

2. **OpenAI Model** *(Required)* – Default is `gpt-4o-mini`. You may choose another supported model like `gpt-5`.

3. **OpenAI API Endpoint** *(Optional)* – Enter your custom API endpoint if you are using a self-hosted model.

4. **Firecrawl API Key** *(Optional)* – Recommended for better website and documentation crawling.

   Click **Submit** to save your configuration.

## Enabling Captain for an Account

After enabling Captain globally, activate it for individual accounts:

1. In the **Super Admin Console**, go to **Accounts**.

2. Select the account you want to enable Captain for and click **Edit**.

3. Under the **Premium Features** section, toggle **Captain** on.

4. Save the changes.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQjRLL1FFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--df5095b551827cac323bd59ce90b30b932a5b50a/Screenshot%202025-08-15%20at%2011.52.31%E2%80%AFAM.png)

## Troubleshooting

If Captain is not responding as expected:

* Verify that the **OpenAI API key** is correct and active.

* Check that the **model name** matches a supported model.

* Ensure your **Firecrawl API key** is valid if using crawling.

* Confirm that Captain is enabled both at the installation and account levels.

If Captain is still not responding, review the Chatwoot server logs for both the web and worker processes to identify any errors, and share those error details with the support team for further assistance.
