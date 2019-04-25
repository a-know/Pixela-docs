---
Title: GET - /v1/users/<username>/graphs
Date: 2019-04-24T06:52:38+09:00
URL: https://pixela-docs.hatenablog.com/entry/get-graph
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/17680117127076483311
---

### Description
Get all predefined pixelation graph definitions.

### HTTP Method , API endpoint
<span class="badge badge-get">GET</span> `/v1/users/<username>/graphs`

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|


### Example

```sh
$ curl -X GET https://pixe.la/v1/users/a-know/graphs -H 'X-USER-TOKEN:thisissecret'
{"graphs":[{"id":"test-graph","name":"graph-name","unit":"commit","type":"int","color":"shibafu","timezone":"Asia/Tokyo","purgeCacheURLs":["https://camo.githubusercontent.com/xxx/xxxx"],"selfSufficient":"increment"}]}
```
