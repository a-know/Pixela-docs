---
Title: DELETE - /v1/users/<username>
Date: 2019-04-23T21:41:49+09:00
URL: https://docs.pixe.la/entry/delete-user
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/17680117127076345877
---

### Description
Deletes the specified registered user.

### HTTP Method , API endpoint
<span class="badge badge-delete">DELETE</span> `/v1/users/<username>`

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|


### Example

```sh
$ curl -X DELETE https://pixe.la/v1/users/a-know -H 'X-USER-TOKEN:thisissecret'
{"message":"Success.","isSuccess":true}
```
