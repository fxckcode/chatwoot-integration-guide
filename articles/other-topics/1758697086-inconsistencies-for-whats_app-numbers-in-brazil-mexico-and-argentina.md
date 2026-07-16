# Inconsistencies for WhatsApp Numbers in Brazil and Argentina

Over the past few years, some countries have changed their mobile numbering systems to accommodate growth. These changes created inconsistencies between the number you can dial today and the number WhatsApp has stored for older accounts.

* **Brazil:** A "9" was added after the area code to all mobile numbers, creating a 13-digit total format. Example: +55 11 9 8765-4321 instead of +55 11 8765-4321.

* **Argentina**:  Numbers may appear with or without a "9" after the country code, depending on when the WhatsApp account was registered. Example: +54 9 11 1234-5678 vs +54 11

  1234-5678.

Because of this, when Chatwoot initiates a WhatsApp conversation (using the “correct” dialable format), WhatsApp may respond with the user’s older registered number. This can create duplicate contacts and disrupt ticket flow in your inbox.

Unfortunately, this issue comes from WhatsApp itself. There is **no fix at the API level**, and it’s unlikely WhatsApp will update old accounts to match the new numbering rules.

## How Chatwoot Solves This

We’ve added logic to automatically prevent duplicate contacts and tickets when these mismatches occur:

* **Case 1: Incoming message with a new-format number**  
  (e.g., `+55` country code + area code + **9** + number, 13 digits total)  
  → No change needed. The message is linked directly to the existing contact.

* **Case 2: Incoming message with an old-format number**  
  (e.g., `+55` country code + area code + number, 12 digits total, missing the extra digit)  
  → Chatwoot checks if a contact already exists in the new format.  
  → If it does, we link the message to the correct contact instead of creating a duplicate.

## What this means for you

* You may still notice the difference in how numbers look in WhatsApp vs how they look in your CRM.

* You can continue messaging customers normally Chatwoot takes care of the background mismatch

* Chatwoot automatically normalizes phone numbers from both old and new formats behind the scenes to ensure consistent contact matching, regardless of which format WhatsApp returns.
