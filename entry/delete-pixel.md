---
Title: DELETE - /v1/users/<username>/graphs/<graphID>/<yyyyMMdd>
Date: 2019-04-24T16:35:08+09:00
URL: https://pixela-docs.hatenablog.com/entry/delete-pixel
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/17680117127076649428
---

### Description
Delete the registered "Pixel".

### HTTP Method , API endpoint
<span class="badge badge-delete">DELETE</span> `/v1/users/<username>/graphs/<graphID>/<yyyyMMdd>`

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|

### Example

```sh
$ curl -X DELETE https://pixe.la/v1/users/a-know/graphs/test-graph/20180915 -H 'X-USER-TOKEN:thisissecret'
{"message":"Success.","isSuccess":true}
```
