---
Title: GET - /v1/users/<username>/webhooks
Date: 2019-04-24T16:38:33+09:00
URL: https://pixela-docs.hatenablog.com/entry/get-webhooks
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/17680117127076650509
---

### Description
Get all predefined webhooks definitions.

### HTTP Method , API endpoint
<span class="badge badge-get">GET</span> `/v1/users/<username>/webhooks`

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|


### Example

```sh
$ curl -X GET https://pixe.la/v1/users/a-know/webhooks -H 'X-USER-TOKEN:thisissecret'
{"webhooks":[{"webhookHash":"<WebhookHashString>","graphID":"test-graph","type":"increment"}]}
```
