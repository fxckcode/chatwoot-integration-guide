# Connecting WhatsApp voice channel

With WhatsApp Calling, customers call your business number straight from the WhatsApp app, and agents answer in their browser. 

**Before you start:**

* The inbox must be a WhatsApp Cloud inbox (the official WhatsApp Cloud API). WhatsApp inboxes connected through other providers (such as 360dialog) can't use calling.

* The phone number must be enrolled in the WhatsApp Business Calling API. If it isn't, turning calling on will fail with a message asking you to onboard the number with Meta (or your WhatsApp Business Solution Provider) first.

**Steps to enable for new inboxes:**

1. In Chatwoot, create  the "WhatsApp Call Channel" inbox — *Settings → Inboxes → Add Inbox → WhatsApp Call*.

   \
   ![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSitzWWdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--b4959180e58e02a0543d7846a3423a5cb16bece7/image.png)

2. Do the embedded signup to complete the voice call integration, once done  the inbox is ready to make and receive calls on that number.

   \
   ![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCS0NzWWdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--9629e45ad93bc19ac724904b7ba04db53e3fdb67/image.png?cw_image_width=751px)

**Steps to enable for existing  inboxes:**

1. Open the inbox's "Calls" settings tab and turn on "Enable Voice Calling". 

   \
   ![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSjZzWWdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--0c3e556fbd9feaaead90e60c26643117a3bde1ad/image.png)

2. If the inbox is connected via embedded signup: toggle the voice call flag. If the inbox is connected via manual keys, ensure that you enable calls web-hook subscription in [developers.facebook.com](http://developers.facebook.com).

   \
   ![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCS0dzWWdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--8f40457f10f6590f9383715ab81a0a990eb408c1/image.png)

**Things to note about permission/consent** 

WhatsApp requires the customer to allow incoming calls. If an agent tries to call someone who hasn't consented yet, Chatwoot sends a permission request instead of placing the call. 

This request shows *"Sent a call permission request to the contact. Try again once they accept."* Once the contact accepts, calls go through normally. (If a request was sent very recently, Chatwoot waits before sending another call request.)

Call permission request message can be updated to send customized message to the user and this is available under the Calls tab under inbox settings.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCQS9IWWdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--1a9671b54f740d75d6c430e563eee42ea1e28c0f/image.png)
