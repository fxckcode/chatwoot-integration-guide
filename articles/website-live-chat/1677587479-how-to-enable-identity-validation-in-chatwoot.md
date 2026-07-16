# How to enable identity validation in Chatwoot?

Identity validation helps ensure that the conversations between your customers and support agents are private. It also helps with disallowing impersonation.

Identity validation can be enabled by generating an HMAC.

The key used to generate HMAC for each web widget differs and can be copied from Inboxes -> Settings -> Configuration -> Identity Validation -> Copy the token shown there.

\
![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCT2hicXdVPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--9c7c1953b95b1b9907e77e07bb0b1f132183eaa4/CleanShot%202026-06-24%20at%2010.40.38@2x.png)

You can generate HMAC in different languages, as shown below.

## Generate HMAC[​](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/identity-validation#generate-hmac "Direct link to heading")

### PHP[**​**](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/identity-validation#php "Direct link to heading")

```
<?php

$key = '<webwidget-hmac-token>';
$message = '<identifier>';

$identifier_hash = hash_hmac('sha256', $message, $key);
?>
```

### Javascript (Node.js)[​](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/identity-validation#javascript-nodejs "Direct link to heading")

```
const crypto = require('crypto');

const key = '<webwidget-hmac-token>';
const message = '<identifier>';

const hash = crypto.createHmac('sha256', key).update(message).digest('hex');
```

### Ruby[**​**](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/identity-validation#ruby "Direct link to heading")

```
require 'openssl'
require 'base64'

key = '<webwidget-hmac-token>'
message = '<identifier>'

OpenSSL::HMAC.hexdigest('sha256', key, message)
```

### Elixir[**​**](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/identity-validation#elixir "Direct link to heading")

```
key = '<webwidget-hmac-token>'
message = '<identifier>'

signature = :crypto.hmac(:sha256, key, message)

Base.encode16(signature, case: :lower)
```

### Golang[**​**](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/identity-validation#golang "Direct link to heading")

```
package main

import (
    "crypto/hmac"
    "crypto/sha256"
    "encoding/base64"
    "encoding/hex"
)

func main() {
  secret := []byte("<webwidget-hmac-token>")
  message := []byte("<identifier>")

  hash := hmac.New(sha256.New, secret)
  hash.Write(message)
  hex.EncodeToString(hash.Sum(nil))
}
```

### Python[**​**](https://www.chatwoot.com/docs/product/channels/live-chat/sdk/identity-validation#python "Direct link to heading")

```
import hashlib
import hmac
import base64

secret = bytes('<webwidget-hmac-token>', 'utf-8')
message = bytes('<identifier>', 'utf-8')

hash = hmac.new(secret, message, hashlib.sha256)
hash.hexdigest()
```

##
