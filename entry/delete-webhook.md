---
Title: DELETE - /v1/users/<username>/webhooks/<webhookHash>
Date: 2019-04-24T16:41:45+09:00
URL: https://docs.pixe.la/entry/delete-webhook
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/17680117127076651657
---

### Description
Delete the registered Webhook.

### HTTP Method , API endpoint
<span class="badge badge-delete">DELETE</span> `/v1/users/<username>/webhooks/<webhookHash>`

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|


### Example

```sh
$ curl -X DELETE https://pixe.la/v1/users/a-know/webhooks/<webhookHash> -H 'X-USER-TOKEN:thisissecret'
{"message":"Success.","isSuccess":true}
```
