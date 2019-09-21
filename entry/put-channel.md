---
Title: PUT - /v1/users/<username>/channels/<channelID>
Date: 2019-09-21T16:45:41+09:00
URL: https://docs.pixe.la/entry/put-channel
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/26006613437567164
---

### Description
Update predefined channel settings.

### HTTP Method , API endpoint
<span class="badge badge-post">PUT</span> `/v1/users/<username>/channels/<channelID>`

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|


### Request Body

|Key|Type|Description|
|---|---|---|
|name|string|[optional] It is the name of the channel settings.|
|type|string|[optional] It is the channel type for notification. Only`slack` is supported.|
|detail|string|[optional] A json string that specifies the details of the `type`.<br>For information about `detail` for each `type', see below table.|

#### `detail` when `type` is `slack`

|Key|Type|Description|
|---|---|---|
|url|string|**[required]** Specifies the URL of the incoming webhook created by slack.|
|userName|string|**[required]** The name of the user to be notified by slack when a notification is made.|
|channelName|string|**[required]** The channel name of the slack to be notified.|

### Example

```sh
$ curl -X PUT https://pixe.la/v1/users/a-know/channels/my-channel -H 'X-USER-TOKEN:thisissecret' -d '{"name":"My slack channel","type":"slack","detail":{"url":"https://hooks.slack.com/services/T035DA4QD/B06LMAV40/xxxx","userName":"Pixela Notification","channelName":"pixela-notify"}}'
{"message":"Success.","isSuccess":true}
```
