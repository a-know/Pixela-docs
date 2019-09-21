---
Title: DELETE - /v1/users/<username>/graphs/<graphID>/notifications/<notificationID>
Date: 2019-09-21T17:16:45+09:00
URL: https://docs.pixe.la/entry/delete-notification
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/26006613437578745
---

### Description
Delete predefined notification settings.

### HTTP Method , API endpoint
<span class="badge badge-delete">DELETE</span> `/v1/users/<username>/graphs/<graphID>/notifications/<notificationID>`

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|

### Example

```sh
$ curl -X DELETE https://pixe.la/v1/users/a-know/graphs/test-graph/notifications/my-notify-rule -H 'X-USER-TOKEN:thisissecret'
{"message":"Success.","isSuccess":true}
```
