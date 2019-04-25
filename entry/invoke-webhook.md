---
Title: POST - /v1/users/<username>/webhooks/<webhookHash>
Date: 2019-04-24T16:40:37+09:00
URL: https://pixela-docs.hatenablog.com/entry/invoke-webhook
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/17680117127076651230
---

### Description
Invoke the webhook registered in advance.<br>
It is used "timezone" setting as post date if Graph's "timezone" is specified, if not specified, calculates it in "UTC".

### HTTP Method , API endpoint
<span class="badge badge-post">POST</span> `/v1/users/<username>/webhooks/<webhookHash>`

### Request Header

|Key|Description|
|---|---|
|Content-Length|Since the request body is not specified, specify the `Content-Length` header.|


### Example

```sh
$ curl -X POST https://pixe.la/v1/users/a-know/webhooks/<webhookHash> -H 'Content-Length:0'
{"message":"Success.","isSuccess":true}
```
