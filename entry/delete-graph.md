---
Title: DELETE - /v1/users/<username>/graphs/<graphID>
Date: 2019-04-24T07:00:26+09:00
URL: https://pixela-docs.hatenablog.com/entry/delete-graph
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/17680117127076485203
---

### Description
Update predefined pixelation graph definitions.<br>The items that can be updated are limited as compared with the pixelation graph definition creation.

### HTTP Method , API endpoint
<span class="badge badge-delete">DELETE</span> `/v1/users/<username>/graphs/<graphID>`

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|

### Example

```sh
$ curl -X DELETE https://pixe.la/v1/users/a-know/graphs/test-graph -H 'X-USER-TOKEN:thisissecret'
{"message":"Success.","isSuccess":true}
```
