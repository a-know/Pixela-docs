---
Title: GET - /v1/users/<username>/channels
Date: 2019-09-21T16:40:08+09:00
URL: https://docs.pixe.la/entry/get-channels
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/26006613437563871
---

### Description
Get all predefined channels.

### HTTP Method , API endpoint
<span class="badge badge-get">GET</span> `/v1/users/<username>/channels`

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|


### Example

```sh
$ curl -X GET https://pixe.la/v1/users/a-know/channels -H 'X-USER-TOKEN:thisissecret'
{"channels":["id":"my-channel","name":"My slack channel","type":"slack","detail":{"url":"https://hooks.slack.com/services/T035DA4QD/B06LMAV40/xxxx","userName":"Pixela Notification","channelName":"pixela-notify"}]}
```
