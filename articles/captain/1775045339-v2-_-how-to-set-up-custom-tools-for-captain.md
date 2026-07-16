# How to Set Up Custom Tools for Captain?

Custom Tools let Captain call your external APIs during conversations — so it can check warranty status, verify service coverage, or fetch data from your own services without handing off to a human agent.

When a customer asks a question, Captain extracts the relevant values from the conversation, inserts them into your API request, and uses the response to form its reply.

Custom Tools is available on the **Business plan** and above.

## Creating a tool

Navigate to **Captain -> Tools** and click **Create a new tool**.\
![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRkNNM1FRPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--df7aee7258ed39aa41dba2b379f759b0ea35e719/image.png)Fill in the following fields:

**Tool Name** — A short name like "Warranty Lookup" or "Service Area Check" (max 55 characters).

**Description** — Tell Captain when to use this tool. This is the most important field. Write it like you're briefing a support agent: "Checks the warranty status of a product by its serial number." Vague descriptions like "Warranty API" will cause Captain to miss opportunities to use the tool.

**Method** — Choose GET (for fetching data) or POST (for submitting data).

**Endpoint URL** — Your API's URL. Use `{{ parameter_name }}` to insert values extracted from the conversation:

`https://api.yourcompany.com/v1/warranty/{{ serial_number }}`

The URL must use HTTPS, must be a hostname (not an IP address), and cannot point to localhost or private networks.

**Authentication** — Choose how your API authenticates requests:

* **None** — No authentication

* **Bearer Token** — Sends your token in the `Authorization` header

* **Basic Auth** — Sends a username and password

* **API Key** — Sends a custom header name and value (e.g., `X-API-Key`)

Authentication credentials are only visible to account administrators.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSHlQM1FRPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--f828a1d2122bd3e56593af9c548c54d0c068a9b5/image.png)

\
**Parameters** — Define what Captain should extract from the customer's message. Each parameter needs a name, type, and description. For example: `serial_number` (String) — "The product serial number, found on the back of the device."

**Request Template** (POST only) — A JSON body template using Liquid syntax.

**Response Template** — Controls what Captain sees from your API's response. If left blank, Captain receives the raw JSON.

Use Liquid to extract relevant fields, for example: `Serial {{ response.serial_number }}: {{ response.warranty_status }}. Expires: {{ response.expiry_date }}.`

Use `response` to access the parsed JSON body. Response templates help Captain focus on the relevant data and avoid internal fields like database IDs or debug info.

## Testing your tool

Click **Test connection** before saving to verify your endpoint is reachable. The test reports the HTTP status code.\
![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQXVUM1FRPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--a68a265c155a8d2863abd67094b035d5ee3c605f/image.png)A green result (HTTP 200–299) means the connection and authentication are working. Note that the test sends the URL without filling in parameter values, so it only verifies that your endpoint is reachable and your credentials are accepted.

If the test fails, check the following:

* 401 Unauthorised — Your authentication credentials are incorrect. Double-check your bearer token, API key, or username/password.

* 403 Forbidden — Your API is rejecting the request. If you require identity verification, note that test requests don't include contact headers.

* 404 Not Found — The endpoint URL is wrong. Verify the path and ensure your API is running.

* Timeout — Your API took too long to respond. Custom tools have a 30-second timeout; make sure your endpoint responds within that window

## Context sent with every tool call

When Captain calls your API, it includes metadata headers so your backend knows the context:

* `X-Chatwoot-Account-Id` — Your account ID

* `X-Chatwoot-Conversation-Id` — The conversation ID

* `X-Chatwoot-Contact-Email` — The customer's email (if available)

* `X-Chatwoot-Contact-Inbox-Verified` — Whether the customer's identity is HMAC-verified

* `X-Chatwoot-Assistant-Id` — The Captain assistant making the call

* `X-Chatwoot-Tool-Slug` — The tool's internal identifier

* `X-Chatwoot-Contact-Id` — The customer's contact ID

* `X-Chatwoot-Contact-Phone` — The customer's phone number (if available)

* `X-Chatwoot-Conversation-Display-Id` — The conversation's display number

You can use these headers to look up the customer in your own system, log which conversations triggered API calls, and verify request authenticity.

## Security

**Built-in protections:**

* All endpoints must use HTTPS

* Requests to private IP ranges, localhost, and `.local` domains are blocked

* HTTP redirects are not followed

* Responses are capped at 1 MB

* Auth credentials are only visible to administrators

**Identity verification:** If your tool returns customer-specific data (orders, billing, account details), your API should check the `X-Chatwoot-Contact-Inbox-Verified` header. Without HMAC verification enabled on your inbox, a visitor could set any email address in the chat widget. Only return sensitive data when this header is `true`. For tools that return public data this check is not needed.

**Prompt injection:** If your API returns user-generated content (reviews, forum posts), malicious text could influence Captain's behavior. Use response templates to extract only structured fields, and sanitize content on your API side.

## Limits

* **Max tools per account** — 15

* **Recommended** — 10 or fewer. A warning appears above 10; more tools make it harder for Captain to pick the right one.

* **Tool name length** — 55 characters

* **Response size** — 1 MB max

* **Request timeout** — 30 seconds

## When to use custom tools

Custom tools are best suited for structured lookups with predictable inputs — checking system status, fetching schedules, or looking up records by ID. If you already have a dedicated Chatwoot integration for your use case (e.g., Shopify for e-commerce), use that instead — dedicated integrations handle search, fuzzy matching, and data sync more reliably than a single API call.

## Examples

### Warranty Lookup

When a customer asks whether their product is still under warranty, Captain can check it using the serial number.

* **Tool Name:** Warranty Lookup

* **Description:** Checks the warranty status of a product by its serial number. Use when a customer asks if their product is covered, when the warranty expires, or what type of coverage they have.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTjJDM1FRPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--a80054243f53a3e776ee0a03230ada57c79f0da8/CleanShot%202026-04-01%20at%2018.40.03@2x.png)

### **Service Area Check**

For businesses that operate in specific regions — customers ask whether service is available at their location.

* **Tool Name:** Service Area Check

* **Description:** Checks whether service or delivery is available in a specific area using the customer's zip code or city name.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCT3lCM1FRPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--de09f1cf35338a45a7d40dd662e2cc0c1d77aa94/CleanShot%202026-04-01%20at%2018.38.23@2x.png)

Custom Tools work best when the inputs are straightforward and the API response is predictable — status checks,  lookups, and other structured queries are a great fit.
