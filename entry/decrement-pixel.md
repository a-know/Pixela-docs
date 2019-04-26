---
Title: PUT - /v1/users/<username>/graphs/<graphID>/decrement
Date: 2019-04-24T16:33:17+09:00
URL: https://docs.pixe.la/entry/decrement-pixel
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/17680117127076648835
---

### Description
Decrement quantity "Pixel" of the day (it is used "timezone" setting if Graph's "timezone" is specified, if not specified, calculates it in "UTC").<br>
If the graph type is int then -1 added, and for float then -0.01 added.

### HTTP Method , API endpoint
<span class="badge badge-put">PUT</span> `/v1/users/<username>/graphs/<graphID>/decrement`

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|
|Content-Length|Since the request body is not specified, specify the `Content-Length` header.|

### Example

```sh
$ curl -X PUT https://pixe.la/v1/users/a-know/graphs/test-graph/decrement -H 'X-USER-TOKEN:thisissecret' -H 'Content-Length:0'
{"message":"Success.","isSuccess":true}
```
