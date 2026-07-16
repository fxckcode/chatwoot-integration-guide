# How to setup an SSL certificate for your Help Center's custom domain?

Using your own domain, like docs.your-company.com, makes your help center feel more trustworthy and on-brand. Chatwoot allows you to use your own custom domain and would help you to secure your site with SSL certificates so that it's safe for your visitors.

This guide walks you through setting up a custom domain for your Help Center portal in Chatwoot.

*Note*: This guide is for Chatwoot Cloud users. If you're using the self-hosted version, you'll need to set up and manage the SSL certificate on your own.

*TLDR: Add your custom domain in Chatwoot portal settings, update your DNS with the CNAME Chatwoot provides, and we will issue the SSL certificate. Once it's ready, your Help Center will be live and accessible to your customers.*

### Step 1: Set up your custom domain in portal settings

Log in to your Chatwoot dashboard and go to the Help Center you want to connect with your custom domain. Click on **Settings**, then scroll to the **Custom Domain** section. Click the **Add custom domain** button to begin the setup.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRUFXN0FFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--6c801bc927770584fb6c8abbc01b95baee85e110/Screenshot-202025-08-07-20at-209.45.06-E2-80-AFAM.png)

You'll now see a prompt asking for your custom domain. Enter the domain where you want your Help Center to be available (e.g., [*docs.yourdomain.com*](http://docs.yourdomain.com)). This is the website address your customers will visit to access your documentation.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRDRXN0FFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--d574d23bce04af1b4ea8afdac2f0b0968de9233a/Screenshot-202025-08-07-20at-209.45.19-E2-80-AFAM.png)

Next, you'll be shown the DNS settings you need to add so we can confirm that the domain is yours and connect it to your Help Center. You’ll need to copy this information and update your DNS provider accordingly.

If you’re not sure how to do it, you can use the option on the screen to email these details to your developer.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRDhXN0FFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--e867de5f9f39bbe76c96a7229d271b42e46b953c/Screenshot-202025-08-07-20at-209.48.12-E2-80-AFAM.png)

### Step 2: Update your DNS with the CNAME record

You must point your custom domain to Chatwoot by creating a CNAME record.

Host: docs  
Type: CNAME  
Value: chatwoot.help

Instructions vary by DNS provider:

#### Using Cloudflare:

You can find the setting under the "DNS" tab.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSGdrN0FFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b9615155f7eec6919cac0af3ee486d5bc205de1d/Screenshot%202025-08-07%20at%2011.00.10%E2%80%AFAM.png)

Note: Make sure that the SSL encryption mode is set to Full in Cloudflare (You can view this under SSL/TLS -> Overview).

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTk1uN0FFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--d8e5534c7d89148e27cf7a6fe69c9ed90b63c661/Screenshot%202025-08-07%20at%2011.12.12%E2%80%AFAM.png)

#### Using AWS Route 53:

You can find the setting under the "Route53" service.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQ1VuN0FFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--2f262ac957b6e041ddc8d2bf8b9178ba0f24ac63/Screenshot%202025-08-07%20at%2011.10.00%E2%80%AFAM.png)

If you're using a different DNS provider, the steps are generally the same. Look for the DNS settings section and add a CNAME record as described. If you’re unsure how to do this, just search for instructions specific to your provider using a phrase like *How to add a CNAME record on [Your DNS Provider]*.

This step links your domain to Chatwoot’s servers. Once it’s done, we’ll have everything we need, your portal details and the domain configuration to issue the SSL certificate and make your Help Center live.

### Step 3: Getting an SSL certificate[​](https://www.chatwoot.com/docs/product/others/help-center/#providing-ssl "Direct link to heading")

Chatwoot provides SSL certificates for all cloud customers on paid plans who set up a custom domain for their Help Center portal.

This step happens automatically. Once you add the CNAME record to your DNS, our server will verify the domain and begin issuing the SSL certificate. This usually takes just a few minutes, but in some cases, depending on your DNS provider and how long they take to update records, it may take up to 24–48 hours.

You can track the status of your SSL certificate right from the Chatwoot dashboard. Initially, you’ll see the status as **Awaiting Verification**. This means we’re still confirming your domain setup before the certificate is issued.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCR29hN0FFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--9980ddd7b9e3b4ec32ada88668f22e0f38508fe2/Screenshot%202025-08-07%20at%2010.22.52%E2%80%AFAM.png)

If there are any issues during the SSL verification process like an incorrect CNAME record or DNS propagation delays, you’ll see an error message next to the status on your dashboard. Hover over the status indicator to view more details about what went wrong and what you need to fix. This helps you quickly identify and resolve any problems in the setup process.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTzhhN0FFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--c9ffebe3e2f3b92a2ac5ddd8913ffebb93236e19/Screenshot%202025-08-07%20at%2010.23.17%E2%80%AFAM.png)

Once the verification is successful and the SSL certificate is issued, the status will change to 'Live' on your dashboard. This means your Help Center is now securely available at your custom domain. Your customers can visit the URL and browse the content.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSG9iN0FFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--05f563a7d45aac5cefa034f3f94bd890282898f7/Screenshot%202025-08-07%20at%2010.22.24%E2%80%AFAM.png)
