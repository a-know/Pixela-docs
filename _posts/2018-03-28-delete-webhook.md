---
category: Webhook
resturi: '/v1/users/&lt;username&gt;/webhooks/&lt;webhookHash&gt;'
title: 'Delete a webhook'
type: 'DELETE'

layout: nil
---

Delete the registered Webhook.

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|


### Example

```$ curl -X DELETE https://pixe.la/v1/users/a-know/webhooks/<webhookHash> -H 'X-USER-TOKEN:thisissecret'
{"message":"Success.","isSuccess":true}```
