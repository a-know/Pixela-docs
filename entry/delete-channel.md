---
Title: DELETE - /v1/users/<username>/channels/<channelID>
Date: 2019-09-21T16:49:02+09:00
URL: https://docs.pixe.la/entry/delete-channel
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/26006613437568146
---

### Description
Delete predefined channel settings.

### HTTP Method , API endpoint
<span class="badge badge-delete">DELETE</span> `/v1/users/<username>/channels/<channelID>`

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|

### Example

```sh
$ curl -X DELETE https://pixe.la/v1/users/a-know/channels/my-channel -H 'X-USER-TOKEN:thisissecret'
{"message":"Success.","isSuccess":true}
```
