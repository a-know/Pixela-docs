---
Title: POST - /v1/users/<username>/channels
Date: 2019-09-21T16:36:39+09:00
URL: https://docs.pixe.la/entry/post-channel
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/26006613437560731
---

### Description
Create a new channel settings for notification.

### HTTP Method , API endpoint
<span class="badge badge-post">POST</span> `/v1/users/<username>/channels`

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|


### Request Body

|Key|Type|Description|
|---|---|---|
|id|string|**[required]** It is an ID for identifying the channel settings.<br>Validation rule: ^[a-z][a-z0-9-]{1,16}|
|name|string|**[required]** It is the name of the channel settings.|
|type|string|**[required]** It is the channel type for notification. Only`slack` is supported.|
|detail|string|**[required]** A json string that specifies the details of the `type`.<br>For information about `detail` for each `type', see below table.|

#### `detail` when `type` is `slack`

|Key|Type|Description|
|---|---|---|
|url|string|**[required]** Specifies the URL of the incoming webhook created by slack.|
|userName|string|**[required]** The name of the user to be notified by slack when a notification is made.|
|channelName|string|**[required]** The channel name of the slack to be notified.|

### Example

```sh
$ curl -X POST https://pixe.la/v1/users/a-know/channels -H 'X-USER-TOKEN:thisissecret' -d '{"id":"my-channel","name":"My slack channel","type":"slack","detail":{"url":"https://hooks.slack.com/services/T035DA4QD/B06LMAV40/xxxx","userName":"Pixela Notification","channelName":"pixela-notify"}}'
{"message":"Success.","isSuccess":true}
```
