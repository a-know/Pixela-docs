---
Title: PUT - /v1/users/<username>/graphs/<graphID>/notifications/<notificationID>
Date: 2019-09-21T17:15:05+09:00
URL: https://docs.pixe.la/entry/put-notification
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/26006613437578232
---

### Description
Update predefined notification rule.



### HTTP Method , API endpoint
<span class="badge badge-post">PUT</span> `/v1/users/<username>/graphs/<graphID>/notifications/<notificationID>`

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|

### Request Body

|Key|Type|Description|
|---|---|---|
|name|string|[optional] It is the name of the notification settings.|
|target|string|[optional] Specify the target to be notified.<br> Only `quantity` is supported.|
|condition|string|[optional] Specify the condition used to judge whether to notify or not.<br>`>`, `=`, `<`, and `multipleOf` are available.<br>You must be a Pixela supporter to specify `multipleOf` condition. see: [https://github.com/a-know/Pixela/wiki/How-to-support-Pixela-by-Patreon-%EF%BC%8F-Use-Limited-Features:title]|
|threshold|string|[optional] Specify the threshold value for deciding whether to notify or not. The number must match the graph type(`int` or `float`).|
|channelID|string|[optional] Specify the ID of the `channel` to be notified.|

### Example

```sh
$ curl -X PUT https://pixe.la/v1/users/a-know/graphs/test-graph/notifications/my-notify-rule -H 'X-USER-TOKEN:thisissecret' -d '{"id":"my-notification-rule","name":"my notification rule","target":"quantity","condition":">","threshold":"5","channelID":"my-channel"}'
{"message":"Success.","isSuccess":true}
```
