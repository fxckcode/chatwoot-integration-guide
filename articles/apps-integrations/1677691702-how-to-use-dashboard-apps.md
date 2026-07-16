# How to use Dashboard Apps?

With Dashboard apps, you can integrate an app within the Chatwoot dashboard for agents' use. This feature enables you to create an application independently, which can then be embedded to provide customers' information, orders, past payment history, etc.

When embedded in Chatwoot's dashboard, your application will get the context of the conversation and contact as a window event. Implement a listener for the message event on your page to receive the context.

P.S. Check out our [YouTube live on building a Dashboard App](https://youtu.be/posSYmbT9H0?list=PL-_vTyAGSIq8t32NtHoR97PAFb-klHUSH&t=123).

## How to create a dashboard app?

**Step 1.** Go to Settings → Integrations → Dashboard apps. Click on the “Configure” button corresponding to the Dashboard Apps.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBNGw1VHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--d7d10a98671c2226a57d43bec26ea8a381f3233b/dashboard%20apps%20feature%20in%20chatwoot.png)

**Step 2.** Add your app name and the URL on which your app is hosted.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBNHg1VHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--59e090bca7a7d20fb3955d9faaf954fa87578b4d/edit%20dashboard%20app.png)

Once you are done, a new tab with the name you gave to the app will appear in the conversation window. In this case, it is “Customer Orders”.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBNDE1VHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--3074634975fc3d3be5c2ffbb5b6538654e807ca2/dashboard%20app%20in%20action.png)

When you click on the new tab, you will be able to see your application fetching data on the Chatwoot dashboard.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBNDU1VHc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--476532e8c8ea7ee21002334c43023af2ef0dfd85/dashboard%20app%20in%20action.png)

### Receiving data from Chatwoot into your app

Chatwoot will deliver the conversation and contact context as a window event. This can be accessed within your app by implementing a listener for the event, as shown here:

```
window.addEventListener("message", function (event) {
  if (!isJSONValid(event.data)) {
    return;
  }

  const eventData = JSON.parse(event.data);
});
```

## On-demand request for data from Chatwoot

If you need to request the conversation data on demand from Chatwoot, you can send a message to the parent window using the javascript [postMessage API](https://developer.mozilla.org/en-US/docs/Web/API/Window/postMessage).

Chatwoot will be listening to this key: `chatwoot-dashboard-app:fetch-info`.

### Example

The following code can be used to query the dashboard app. Chatwoot will respond to this request by providing the updated conversation payload promptly.

```
window.parent.postMessage('chatwoot-dashboard-app:fetch-info', '*')

// You would get a message in the on message listener with the appContext payload.
```

## Event Payload

### conversation object[​](https://www.chatwoot.com/docs/product/others/dashboard-apps/#conversation-object "Direct link to heading")

```
{
  "meta": {
    "sender": {
      "additional_attributes": {
        "description": "string",
        "company_name": "string",
        "social_profiles": {
          "github": "string",
          "twitter": "string",
          "facebook": "string",
          "linkedin": "string"
        }
      },
      "availability_status": "string",
      "email": "string",
      "id": "integer",
      "name": "string",
      "phone_number": "string",
      "identifier": "string",
      "thumbnail": "string",
      "custom_attributes": "object",
      "last_activity_at": "integer"
    },
    "channel": "string",
    "assignee": {
      "id": "integer",
      "account_id": "integer",
      "availability_status": "string",
      "auto_offline": "boolean",
      "confirmed": "boolean",
      "email": "string",
      "available_name": "string",
      "name": "string",
      "role": "string",
      "thumbnail": "string"
    },
    "hmac_verified": "boolean"
  },
  "id": "integer",
  "messages": [
    {
      "id": "integer",
      "content": "Hello",
      "inbox_id": "integer",
      "conversation_id": "integer",
      "message_type": "integer",
      "content_type": "string",
      "content_attributes": {},
      "created_at": "integer",
      "private": "boolean",
      "source_id": "string",
      "sender": {
        "additional_attributes": {
          "description": "string",
          "company_name": "string",
          "social_profiles": {
            "github": "string",
            "twitter": "string",
            "facebook": "string",
            "linkedin": "string"
          }
        },
        "custom_attributes": "object",
        "email": "string",
        "id": "integer",
        "identifier": "string",
        "name": "string",
        "phone_number": "string",
        "thumbnail": "string",
        "type": "string"
      }
    }
  ],
  "account_id": "integer",
  "additional_attributes": {
    "browser": {
      "device_name": "string",
      "browser_name": "string",
      "platform_name": "string",
      "browser_version": "string",
      "platform_version": "string"
    },
    "referer": "string",
    "initiated_at": {
      "timestamp": "string"
    }
  },
  "agent_last_seen_at": "integer",
  "assignee_last_seen_at": "integer",
  "can_reply": "boolean",
  "contact_last_seen_at": "integer",
  "custom_attributes": "object",
  "inbox_id": "integer",
  "labels": "array",
  "muted": "boolean",
  "snoozed_until": null,
  "status": "string",
  "timestamp": "integer",
  "unread_count": "integer",
  "allMessagesLoaded": "boolean",
  "dataFetched": "boolean"
}
```

### contact object[​](https://www.chatwoot.com/docs/product/others/dashboard-apps/#contact-object "Direct link to heading")

```
{
  "additional_attributes": {
    "description": "string",
    "company_name": "string",
    "social_profiles": {
      "github": "string",
      "twitter": "string",
      "facebook": "string",
      "linkedin": "string"
    }
  },
  "availability_status": "string",
  "email": "string",
  "id": "integer",
  "name": "string",
  "phone_number": "+91 9000000001",
  "identifier": "string || null",
  "thumbnail": "+91 9000000001",
  "custom_attributes": {},
  "last_activity_at": "integer"
}
```

### currentAgent object[​](https://www.chatwoot.com/docs/product/others/dashboard-apps/#currentagent-object "Direct link to heading")

```
{
  "email": "string",
  "id": "integer",
  "name": "string"
}
```

### Final Payload[​](https://www.chatwoot.com/docs/product/others/dashboard-apps/#final-payload "Direct link to heading")

```
{
  "event": "appContext",
  "data": {
    "conversation": {
      // <...Conversation Attributes>
    },
    "contact": {
      // <...Contact Attributes>
    },
    "currentAgent": {
      // <...Current agent Attributes>
    }
  }
}
```
