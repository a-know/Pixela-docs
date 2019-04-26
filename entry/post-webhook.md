---
Title: POST - /v1/users/<username>/webhooks
Date: 2019-04-24T16:36:57+09:00
URL: https://docs.pixe.la/entry/post-webhook
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/17680117127076650011
---

### Description
Create a new Webhook.

### HTTP Method , API endpoint
<span class="badge badge-post">POST</span> `/v1/users/<username>/webhooks`

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

```sh
$ curl -X POST https://pixe.la/v1/users/a-know/webhooks -H 'X-USER-TOKEN:thisissecret' -d '{"graphID":"test-graph","type":"increment"}'
{"webhookHash":"<WebhookHashString>","message":"Success.","isSuccess":true}
```
