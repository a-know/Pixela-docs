---
category: Webhook
resturi: '/v1/users/&lt;username&gt;/webhooks'
title: 'Get webhooks'
type: 'GET'

layout: nil
---

Get all predefined webhooks definitions.

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|


### Example

```$ curl -X GET https://pixe.la/v1/users/a-know/webhooks -H 'X-USER-TOKEN:thisissecret'
{"webhooks":[{"webhookHash":"<WebhookHashString>","graphID":"test-graph","type":"increment"}]}```
