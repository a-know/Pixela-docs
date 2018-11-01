---
category: Webhook
resturi: '/v1/users/&lt;username&gt;/webhooks'
title: 'Create a webhook'
type: 'POST'

layout: nil
---

Create a new Webhook.

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|


### Request Body

|Key|Type|Description|
|---|---|---|
|graphID|string|**[required]** Specify the target graph as an ID.|
|type|string|**[required]** Specify the behavior when this Webhook is invoked.<br>Only `increment` or `decrement` are supported.|


### Example

```$ curl -X POST https://pixe.la/v1/users/a-know/webhooks -H 'X-USER-TOKEN:thisissecret' -d '{"graphID":"test-graph","type":"increment"}'
{"hashString":"<WebhookHashString>","message":"Success.","isSuccess":true}```
