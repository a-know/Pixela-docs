---
Title: PUT - /v1/users/<username>/graphs/<graphID>/increment
Date: 2019-04-24T16:31:28+09:00
URL: https://pixela-docs.hatenablog.com/entry/increment-pixel
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/17680117127076648185
---

### Description
Increment quantity "Pixel" of the day (it is used "timezone" setting if Graph's "timezone" is specified, if not specified, calculates it in "UTC").<br>
If the graph type is int then 1 added, and for float then 0.01 added.

### HTTP Method , API endpoint
<span class="badge badge-put">PUT</span> `/v1/users/<username>/graphs/<graphID>/increment`

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|
|Content-Length|Since the request body is not specified, specify the `Content-Length` header.|

### Example

```sh
$ curl -X PUT https://pixe.la/v1/users/a-know/graphs/test-graph/increment -H 'X-USER-TOKEN:thisissecret' -H 'Content-Length:0'
{"message":"Success.","isSuccess":true}
```
