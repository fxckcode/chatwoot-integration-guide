# How to setup a WebSocket connection?

WebSockets establish a continuous connection between the client and server, enabling bi-directional communication. Chatwoot utilizes this connection to provide real-time updates about platform events. To connect to the Chatwoot WebSocket, simply provide a token and follow the setup instructions outlined in this guide.

**Note**: This feature is experimental, and the documentation may change with each release. Additionally, backward compatibility cannot be guaranteed, so it is important to ensure you are using the latest version of the implementation.

## Why should I use a WebSocket connection?

A WebSocket connection allows for real-time data updates, making it ideal for clients such as an Android or iOS client SDK for Chatwoot. This helps update the dashboard without the need to reload the page. Hence, it can enhance the user experience and improve an agent's productivity.

## How to set up a WebSocket connection with Chatwoot?

To set up a WebSocket connection with Chatwoot, you need to initiate a connection with the authentication PubSub token provided by Chatwoot. The URL for the connection is `wss://<your-installation-url>/cable`. If you are using Chatwoot Cloud, you can use `wss://app.chatwoot.com/cable` as the URL.

> A PubSub token is a token that is used to authenticate a client when connecting to a PubSub (publish-subscribe) service. The client must present this token to the service in order to establish a connection and begin publishing or subscribing to messages.

There are two types of PubSub tokens available in Chatwoot, as listed below.

1. **User PubSub Token**: This token has the privileges of an agent/admin and would receive all of the events listed later on the page. You can get the PubSub token by calling the [Profile API](https://www.chatwoot.com/developers/api/#operation/fetchProfile).

2. **Contact PubSub Token**: Chatwoot generates a unique PubSub token for each session a contact has. This token can be used to connect to the WebSocket and receive real-time updates for the same session. When a contact is created through the public APIs, the `pubsub_token` is included in the response payload. This token only grants access to events related to the current session, such as `conversation.created`,  `conversation.status_changed`, `message.created`, `message.updated`, `conversation_typing_on`, `conversation_typing_off` and `presence.update`.

Please refer [Client APIs](https://www.chatwoot.com/docs/product/channels/api/client-apis) to build real time customer facing integrations using Chatwoot.

**Note**: This token may be rotated regularly based on your installation type. Please ensure that you are using the latest token.

### How to connect to Chatwoot WebSocket?

To connect to the Chatwoot WebSocket, use the command `subscribe` and include your `pubSubToken`, `accountId`, and `userId` (if using a user token) in the connection request. Here is an example of how you can connect with Chatwoot.

```
// Add a helper method to convert JSON to a string
const stringify = (payload = {}) => JSON.stringify(payload);

const pubSubToken = "<contact/user-pub-sub-token>";
const accountId = "<your-account-id-in-integer>";
const userId = "<user-id-in-integer-if-using-user-token>";
const connection = new WebSocket(
  "wss://app.chatwoot.com/cable"
);

connection.send(
  stringify({
    command: "subscribe",
    identifier: stringify({
      channel: "RoomChannel",
      pubsub_token: pubSubToken,
      account_id: accountId,
      user_id: userId,
    }),
  })
);

// The expected string in connection.send is of the format:
// {"command":"subscribe","identifier":"{\\"channel\\":\\"RoomChannel\\",\\"pubsub_token\\":\\"your-pubsub-token\\",\\"account_id\\": account_id_integer,\\"user_id\\":user_id_integer }"}
```

### Publishing presence to the WebSocket server

To keep your users’ status online in Chatwoot, you can send a presence update event to Chatwoot every 30 seconds. This action would keep the status of the agent/contact online.

**How to update the presence of an agent/admin?**

To update the presence of an agent or admin, send the following payload to the server:

```
const userPayload = stringify({
  command: "message",
  identifier: stringify({
    channel: "RoomChannel",
    pubsub_token: "<user-pubsub-token>",
    account_id: accountId,
    user_id: userId,
  }),
  data: stringify({ action: "update_presence" }),
});

connection.send(userPayload);
// The expected string in connection.send is of the format:
// {"command":"message","identifier":"{\\"channel\\":\\"RoomChannel\\",\\"pubsub_token\\":\\"your-pubsub-token\\",\\"account_id\\": account_id_integer,\\"user_id\\":user_id_integer ","data":"{\\"action\\":\\"update_presence\\"}"}
```

**How to update the presence of a contact?**

To update the presence of a contact, send the following payload to the server:

```
const agentPayload = stringify({
  command: "message",
  identifier: stringify({
    channel: "RoomChannel",
    pubsub_token: "<user-pubsub-token>",
  }),
  data: stringify({ action: "update_presence" }),
});

connection.send(agentPayload);
// The expected string in connection.send is of the format:
// {"command":"message","identifier":"{\\"channel\\":\\"RoomChannel\\",\\"pubsub_token\\":\\"your-pubsub-token\\","data":"{\\"action\\":\\"update_presence\\"}"}
```

## WebSocket Payload

### Objects

An event can contain any of the following objects as payload. Different types of objects supported in Chatwoot are as follows.

**Conversation**

The following payload will be returned for a conversation.

```
{
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
      "timestamp": "iso-datetime"
    }
  },
  "can_reply": "boolean",
  "channel": "string",
  "id": "integer",
  "inbox_id": "integer",
  "contact_inbox": {
    "id": "integer",
    "contact_id": "integer",
    "inbox_id": "integer",
    "source_id": "string",
    "created_at": "datetime",
    "updated_at": "datetime",
    "hmac_verified": "boolean"
  },
  "messages": ["Array of message objects"],
  "meta": {
    "sender": {
      // Contact Object
    },
    "assignee": {
      // User Object
    }
  },
  "status": "string",
  "unread_count": "integer",
  "agent_last_seen_at": "unix-timestamp",
  "contact_last_seen_at": "unix-timestamp",
  "timestamp": "unix-timestamp",
  "account_id": "integer"
}
```

**Contact**

The following payload will be returned for a contact.

```
{
  "additional_attributes": "object",
  "custom_attributes": "object",
  "email": "string",
  "id": "integer",
  "identifier": "string or null",
  "name": "string",
  "phone_number": "string or null",
  "thumbnail": "string"
}
```

**User**

The following payload will be returned for an agent/admin.

```
{
  "id": "integer",
  "name": "string",
  "available_name": "string",
  "avatar_url": "string",
  "availability_status": "string",
  "thumbnail": "string"
}
```

**Message**

The following payload will be returned for a message.

```
{
  "id": "integer",
  "content": "string",
  "account_id": "integer",
  "inbox_id": "integer",
  "message_type": "integer",
  "created_at": "unix-timestamp",
  "updated_at": "datetime",
  "private": "boolean",
  "status": "string",
  "source_id": "string / null",
  "content_type": "string",
  "content_attributes": "object",
  "sender_type": "string",
  "sender_id": "integer",
  "external_source_ids": "object",
  "sender": {
    "type": "string - contact/user"
    // User or Contact Object
  }
}
```

**Notification**

The following payload will be returned for a notification.

```
{
  "id": "integer",
  "notification_type": "string",
  "primary_actor_type": "string",
  "primary_actor_id": "integer",
  "primary_actor": {
    "can_reply": "boolean",
    "channel": "string",
    "id": "integer",
    "inbox_id": "integer",
    "meta": {
      "assignee": {
        "id": "integer",
        "name": "string",
        "available_name": "string",
        "avatar_url": "string",
        "type": "user",
        "availability_status": "string",
        "thumbnail": "string"
      },
      "hmac_verified": "boolean"
    },
    "agent_last_seen_at": "unix-timestamp",
    "contact_last_seen_at": "unix-timestamp",
    "timestamp": "unix-timestamp",
  },
  "read_at": "unix-timestamp",
  "secondary_actor": "object/null",
  "created_at":"unix-timestamp",
  "account_id": "integer",
  "push_message_title": "string"
}
```

### Identifier

Each event will have an `identifier` attribute in the following format.

```
{
  "identifier": "{\\"channel\\":\\"RoomChannel\\",\\"pubsub_token\\":\\"token\\",\\"account_id\\":id,\\"user_id\\":user_id}"
}
```

### Message

Each event will include a `message` attribute which we return the event name as well as the data associated with it. To see the list of events, refer the documentation below.

## Types of Events

### conversation.created

This event is triggered when a new conversation is initiated. If subscribing to the contact's PubSub token, this event will only include data related to the specific session associated with the PubSub token.

**Available to**: agent/admin, contact

```
{
  "message": {
    "event": "conversation.created",
    "data": {
      // Conversation object will be available here
    }
  }
}
```

### conversation.read

This event is triggered and sent to the agents/admins who have access to the inbox, when a contact has read a message.

**Available to**: agent/admin

```
{
  "message": {
    "event": "conversation.read",
    "data": {
      // Conversation object will be available here
    }
  }
}
```

### message.created

This event is triggered and sent to the agents, admins, contacts when a new message is created in a conversation they have access to.

**Available to**: agent/admin, contact

```
{
  "message": {
    "event": "message.created",
    "data": {
      // Message object will be available here
    }
  }
}
```

### message.updated

This event is triggered and sent to the agents, admins, contacts when a message is updated in a conversation they have access to.

**Available to**: agent/admin, contact

```
{
  "message": {
    "event": "message.updated",
    "data": {
      // Message object will be available here
    }
  }
}
```

### conversation.status_changed

This event is sent to the agents, admins, contacts when a conversation status is updated.

**Available to**: agent/admin, contact

```
{
  "message": {
    "event": "conversation.status_changed",
    "data": {
      // Conversation object will be available here
    }
  }
}
```

### conversation.typing_on

This event is sent to the agents, admins, contacts when a contact or an agent starts typing a response.

**Available to**: agent/admin, contact

```
{
  "message": {
    "event": "conversation.typing_on",
    "data": {
      "conversation": {
        // Conversation object will be available here
      },
      "user": {
        // Contact / Agent,Admin User object will be available here.
      },
      "is_private": "boolean", // Shows whether the agent is typing a private note or not.
      "account_id": "integer"
    }
  }
}
```

### conversation.typing_off

This event is sent to the agents, admins, contacts when a contact or an agent ends typing a response.

**Available to**: agent/admin, contact

```
{
  "message": {
    "event": "conversation.typing_off",
    "data": {
      "conversation": {
        // Conversation object will be available here
      },
      "user": {
        // Contact / User object will be available here.
      },
      "account_id": "integer"
    }
  }
}
```

### assignee.changed

This event is sent to the agents/admins with access to an inbox when the assigned agent is changed.

**Available to**: agent/admin

```
{
  "message": {
    "event": "assignee.changed",
    "data": {
      // Conversation object will be available here
    }
  }
}
```

### team.changed

This event is sent to the agents/admins with access to an inbox when the assigned team is changed.

**Available to**: agent/admin

```
{
  "message": {
    "event": "team.changed",
    "data": {
      // Conversation object will be available here
    }
  }
}
```

### conversation.contact_changed

This event is sent to the agents/admins when two contacts are merged all their conversations are consolidated under one contact.

**Available to**: agent/admin

```
{
  "message": {
    "event": "conversation.contact_changed",
    "data": {
      // Conversation object will be available here
    }
  }
}
```

### contact.created

This event is sent to the agents/admins when a contact is created.

**Available to**: agent/admin

```
{
  "message": {
    "event": "contact.created",
    "data": {
      // Contact object will be available here
    }
  }
}
```

### contact.updated

This event is sent to the agents/admins when a contact is updated.

**Available to**: agent/admin

```
{
  "message": {
    "event": "contact.updated",
    "data": {
      // Contact object will be available here
    }
  }
}
```

### presence.update

Available for both agent and the contact, this event provides real-time updates on the availability status of the users in the system. The event delivered to contacts will not include information about other contacts' availability status.

**Available to**: agent/admin

```
{
  "message": {
    "event": "presence.update",
    "data": {
      "account_id": "integer",
      "users": {
        "user-id": "string"
      },
      "contacts": {
        "contact-id": "string"
      }
    }
  }
}
```

### notification_created

This event is sent to the agents/admins when a notification is created.

**Available to**: agent/admin
