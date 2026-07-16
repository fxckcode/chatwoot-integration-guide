# Voice Calling in Chatwoot

Talk to your customers by voice, right from the same inbox where you already handle chats. This guide is in three parts:

1. **What voice calling is and how it helps**: overview on voice calling feature

2. **Connecting a voice channel**: setup for each provider (Twilio and WhatsApp)

3. **Using voice calling day to day**: answering, assignments, who gets rung, and what happens after a call

---

## 1. What voice calling is and how it helps

Voice calling lets your agents make and receive phone calls inside Chatwoot, without juggling a separate phone app. A call lives in the same place as the rest of the conversation, so the chat history, contact details, notes, and the call all sit together in one timeline.

### 1.1. Why teams use it

* **One screen for everything.** When a customer calls, the agent already sees who they are and what they've talked about before, no asking them to repeat themselves.

* **No phones to manage.** Agents talk through their browser using a headset or the computer's mic and speakers. There's no additional overhead of any new softwares or browser extensions.

* **Every call is on the record.** Each call automatically becomes a message in the conversation, showing whether it was answered, how long it lasted, who picked it up, and, when available, a recording you can replay and a written transcript you can read.

* **The team shares the load.** An incoming call rings the right available agents at once, so customers reach a real person quickly.

### 1.2. Different ways to receive a call

Chatwoot supports voice through two providers. You can use either or both:

| Provider             | Best for                          | How the customer reaches you                                  |
| -------------------- | --------------------------------- | ------------------------------------------------------------- |
| **Twilio Voice**     | A traditional business phone line | Customer dials your phone number from any phone               |
| **WhatsApp Calling** | Businesses already on WhatsApp    | Customer taps "call" on your business inside the WhatsApp app |

> **Note:** Voice calling is a premium feature. It must be enabled on your account (the **Voice Channel** feature) before the options below appear. If you don't see voice settings, contact your account admin or your Chatwoot provider.

---

## 2. Connecting a voice channel

Setting up voice is an admin task, done once per inbox. Pick the section that matches the provider you want.

### 2.1. Twilio Voice (a phone-number line)

Please follow along this article to setup Twilio Voice: [Connecting Twilio voice channel](https://www.chatwoot.com/hc/user-guide/articles/1779871614-connecting-twilio-voice-channel )

### 2.2. WhatsApp Calling

Please follow along this article to setup WhatsApp Calling: [Connecting WhatsApp voice channel](https://www.chatwoot.com/hc/user-guide/articles/1779871708-connecting-whats_app-voice-channel) 

One requirement for agents: their browser must have microphone permission granted for Chatwoot.

---

## 3. Using voice calling day to day

Once an inbox has voice enabled, calling works the same way for agents no matter which provider is behind it.

### 3.1. Receiving an incoming call

When a customer calls, a floating call widget pops up in the corner of the screen for the agents who should answer, and a ringtone plays. The card shows the caller's name, number, and (when known) their location, plus which channel the call came in on.

From that widget an agent can:

* **Join call**: answer and start talking by clicking the green call accept button.

* **Reject**: decline the call (the caller is no longer ringing this agent) by clicking the red call reject button.

* **Dismiss**: quietly hide the popup on this screen without rejecting the call, so other agents can still pick it up. You can do this by clicking the cross button on the top right of the widget.

If a teammate (or the same agent in another browser tab) has already grabbed the call, the widget shows "Being handled in another tab" so two people don't answer the same call.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQnEyWWdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--a636bfb93b647672c76979eaeba0343a320fdc0c/image-1%20copy.png?cw_image_width=737px)

While connected, the widget shows a running timer and these controls:

* **Mute mic / Unmute mic**: turn the agent's microphone off and on by clicking in the green mic button.

* **End call**: hang up by clicking on the red call end button.

* **Go to conversation thread / View chat history**: jump to the full conversation while staying on the call by clicking on the "Go to conversation thread" link at the bottom of the widget. This makes it easier for the agent can see the previous history of the conversation or get more details about the contact.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTjYzWWdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--ef732c9ad84def72b3c0d5b49a1c12a674ebe64b/image-2.png)

### 3.2. Notification and call assignments

Chatwoot rings the people most likely to help, it does not ring everyone blindly. For an incoming call, it rings in this order of priority:

1. **The assigned agent**, if the conversation already has one, only they are rung.

2. **Otherwise, the online agents in that inbox**, everyone who is available gets the call notification at once.

3. **Otherwise, all online admins on the account**, a last resort so no call goes unanswered.

A few rules that follow from this:

* **Only available (online) agents get a ringing popup** for incoming calls. Agents who are offline or busy are skipped.

* **First to answer wins.** There's no queue or round-robin, whoever picks up first takes the call, and for the others it stop ringing and the call notification goes away.

* **The call is auto-assigned to whoever answers.** The conversation becomes theirs, so follow-up stays with the person who handled it.

* **Outbound calls** always belong to the agent who started them.

### 3.3. Call states (what the labels mean)

Every call moves through a simple lifecycle, and the conversation reflects it:

| What you see                             | Meaning                                  |
| ---------------------------------------- | ---------------------------------------- |
| **Incoming call / Outgoing call**        | The call is ringing                      |
| **Call in progress**                     | Connected and talking                    |
| **Call ended**                           | Finished normally                        |
| **No answer** (*Contact didn't pick up)* | Outbound call the customer didn't answer |
| **Missed call** (*No agent picked up)*   | Incoming call nobody answered            |
| **Declined by {agent}**                  | An agent rejected the call               |

### 3.4. After the call

When a call ends, it's saved as a call entry in the conversation timeline, so there's a permanent record. Depending on your setup, that entry can include:

* **Call summary**: Direction (incoming/outgoing), the final status, how long it lasted, and which agent answered (e.g. *"You answered"*, *"{agent} answered"*, or *"They answered"*).

* **Recording**: For Twilio calls a recording is captured automatically and attached so you can replay it. For WhatsApp calls a recording is attached when it is available.

* **Transcript**: If your account has AI transcription enabled (the Captain integration, subject to available quota), the recording is turned into readable text right inside the call entry, with a `Show more / Show less` toggle for long calls.

  \
  ![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRHlBWWdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--2e52f6712f7da8dd37cb04fc3141b2681c4a8ffd/image.png)

A missed or declined call still leaves an entry (e.g. Missed call - No agent picked up), and the agent can use Call back from the conversation to return it.

### 3.5 Starting an outbound call

When an agent misses a call, Chatwoot provides the ability to seamlessly do a callback to the customer from the dashboard. From inside a conversation, the agent can use the call button in the conversation header:

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQkN6WWdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--c319e548ca9960710fd6d8e855e18c992f2ebb9b/image.png)

You can also start a call from the contact info screen also.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQ0REWWdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--7b1aca24fb22c1bbd90400be703d6bc495546fab/Screenshot%202026-05-27%20at%203.16.55%E2%80%AFPM.png?cw_image_width=386px)

---

### Quick troubleshooting

* **No voice settings appear.** The Voice Channel feature isn't enabled on your account — ask your admin or Chatwoot provider.

* **WhatsApp calling won't turn on.** The number isn't enrolled in the WhatsApp Business Calling API yet, or the inbox isn't a WhatsApp Cloud inbox. Onboard the number with Meta / your provider and try again.

* **The call connects but there's no sound, or it won't start.** Check hat the browser has microphone permission for Chatwoot, and that a headset/mic is selected.

* **A customer says they can't call your WhatsApp number.** They may not have accepted the call permission request yet — they'll get one when an agent tries to call, and calls work once they accept.
