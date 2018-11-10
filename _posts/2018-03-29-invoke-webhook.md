---
category: Webhook
resturi: '/v1/users/&lt;username&gt;/webhooks/&lt;webhookHash&gt;'
title: 'Invoke webhooks'
type: 'POST'

layout: nil
---

Invoke the webhook registered in advance.<br>
It is used "timezone" setting as post date if Graph's "timezone" is specified, if not specified, calculates it in "UTC".

### Request Header

|Key|Description|
|---|---|
|Content-Length|Since the request body is not specified, specify the `Content-Length` header.|


### Example

```$ curl -X POST https://pixe.la/v1/users/a-know/webhooks/<webhookHash> -H 'Content-Length:0'
{"message":"Success.","isSuccess":true}```
