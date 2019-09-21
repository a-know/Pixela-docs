---
Title: GET - /v1/users/<username>/graphs/<graphID>/notifications
Date: 2019-09-21T17:11:53+09:00
URL: https://docs.pixe.la/entry/get-notifications
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/26006613437577170
---

### Description
Get all predefined notifications.

### HTTP Method , API endpoint
<span class="badge badge-get">GET</span> `/v1/users/<username>/graphs/<graphID>/notifications`

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|


### Example

```sh
$ curl -X GET https://pixe.la/v1/users/a-know/graphs/test-graph/notifications -H 'X-USER-TOKEN:thisissecret'
{"notifications":["id":"my-notify-rule","name":"my notify rule","target":"quantity","condition":">","threshold":"5","channelID":"my-channel"]}
```
