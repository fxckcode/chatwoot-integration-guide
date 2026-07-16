# Connecting Twilio voice channel

With Twilio Voice, customers call a real phone number and agents answer in their browser. 

What you'll need from your Twilio account:

* Account SID and Auth Token

* An API Key SID and API Key Secret (secure tokens to connect each agent to the call)

* A TwiML App and a Twilio phone number

## Steps to create a new Voice Channel inbox

1. In Chatwoot, create (or open) the "Voice Channel" inbox — *Settings → Inboxes → Add Inbox → Voice Channel*.

   \
   ![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQW1zWWdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--279d44246aac936d5a9d7c0d9620a7d3bc97ca95/image.png?cw_image_width=522px)

2. Enter your Twilio phone number and the Twilio credentials above, enter your "API Key SID" and "API Key Secret", then save. 

   \
   ![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQXVzWWdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--c38c1031ef67dacbfcaa921b673025750f0e4427/image.png?cw_image_width=818px)

3. Chatwoot will then show you two URLs:

   * Twilio Voice URL

   * Twilio Status Callback URL

4. Copy those and update it in the Twilio Dashboard: paste the "Twilio Voice URL" onto both your Twilio phone number settings and your TwiML App, and paste the "Twilio Status Callback URL" onto your phone number's status callback field.

## Steps to enable Voice in existing inboxes

1. Got to your inbox's settings page. (Settings > Inboxes > {Inbox Name})

2. Open the inbox's "Voice" settings tab and turn on radio button labeled "Enable Voice Calling".

3. Chatwoot will then show you two URLs:

   * Twilio Voice URL

   * Twilio Status Callback URL

4. Copy those and update it in the Twilio Dashboard: paste the "Twilio Voice URL" onto both your Twilio phone number settings and your TwiML App, and paste the "Twilio Status Callback URL" onto your phone number's status callback field.

   \
   ![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQWlzWWdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--2a75ce39520ce550b4a092314ec9a6727a98df12/image.png?cw_image_width=534px)  

   

5. Once saved, the inbox is ready to make and receive calls on that number.
