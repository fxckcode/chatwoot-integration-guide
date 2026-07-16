# How to use template variables?

With template variables, you can personalize your messages by inserting dynamic content tailored to each recipient. By adding placeholders in your messages, you can easily customize your communications with information such as a customer's name, order number, or other details.

For e.g., If you send a message `Hey {{ contact.name }}, how may I help you?`, Chatwoot will pick the contact name and send a message like `Hey John, how may I help you?`.

You can also utilize variables in [canned responses](https://app.chatwoot.com/hc/chatwoot-user-guide-cloud-version/en/features-explained/469), macros, and [automation](https://app.chatwoot.com/hc/chatwoot-user-guide-cloud-version/en/advanced-features-explained/496).

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBMFp1VVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--adf82e3fc0093e1a2d2b17eeac1b9fc4fe2c01b6/template%20varibales%20in%20chatwoot.png)

## Creating template variables

To use a variable, type two double curly brackets **{{** when composing a new message or creating a canned response. The variables will appear, and you can select the one you'd like to use.

The available template variables are:

* [conversation.id](http://conversation.id)

  \~ For the numeric version of the conversation ID.

* [contact.id](http://contact.id)

  \~ For the numeric version of the contact ID.

* [contact.name](http://contact.name)

  \~ For the contact's full name.

* contact.first_name

* contact.last_name

* contact.phone_number

* [agent.name](http://agent.name)

* agent.first_name

* agent.last_name

* agent.phone_number

### What if I send a non-existent variable?

If you try to send an undefined variable, Chatwoot will show a warning.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBNWx1VVE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--4da7b500d43072f5c04bedf43b4dea5e9a402a40/undefined%20variable%20warning.png)

### How to add a fallback text?

If a defined variable cannot be populated by the system, a fallback text can be used to replace the intended value. For e.g., if the variable `contact.first_name` cannot be populated, a suitable fallback text could be 'there'.

When defining a fallback text, make sure you surround it with single quotes. Here is an example: `{{ contact.first_name || 'there'}}`.
