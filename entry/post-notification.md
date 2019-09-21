---
Title: POST - /v1/users/<username>/graphs/<graphID>/notifications
Date: 2019-09-21T17:09:42+09:00
URL: https://docs.pixe.la/entry/post-notification
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/26006613437576415
---

### Description
Create a notification rule.<br>You must be a Pixela supporter to create multiple notifications. see: [https://github.com/a-know/Pixela/wiki/How-to-support-Pixela-by-Patreon-%EF%BC%8F-Use-Limited-Features:title]



### HTTP Method , API endpoint
<span class="badge badge-post">POST</span> `/v1/users/<username>/graphs/<graphID>/notifications`

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|

### Request Body

|Key|Type|Description|
|---|---|---|
|id|string|**[required]** It is an ID for identifying the notification settings.<br>Validation rule: ^[a-z][a-z0-9-]{1,16}|
|name|string|**[required]** It is the name of the notification settings.|
|target|string|**[required]** Specify the target to be notified.<br> Only `quantity` is supported.|
|condition|string|**[required]** Specify the condition used to judge whether to notify or not.<br>`>`, `=`, `<`, and `multipleOf` are available.<br>You must be a Pixela supporter to specify `multipleOf` condition. see: [https://github.com/a-know/Pixela/wiki/How-to-support-Pixela-by-Patreon-%EF%BC%8F-Use-Limited-Features:title]|
|threshold|string|**[required]** Specify the threshold value for deciding whether to notify or not. The number must match the graph type(`int` or `float`).|
|channelID|string|**[required]** Specify the ID of the `channel` to be notified.|

### Example

```sh
$ curl -X POST https://pixe.la/v1/users/a-know/graphs/test-graph/notifications -H 'X-USER-TOKEN:thisissecret' -d '{"id":"my-notification-rule","name":"my notification rule","target":"quantity","condition":">","threshold":"5","channelID":"my-channel"}'
{"message":"Success.","isSuccess":true}
```
