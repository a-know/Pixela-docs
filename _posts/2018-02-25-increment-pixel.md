---
category: Pixel
resturi: '/v1/users/&lt;username&gt;/graphs/&lt;graphID&gt;/increment'
title: 'Increment a Pixel'
type: 'PUT'

layout: nil
---

Increment quantity "Pixel" of the day (UTC).<br>If the graph type is int then 1 added, and for float then 0.01 added.

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|
|Content-Length|Since the request body is not specified, specify the `Content-Length` header.|

### Example

```$ curl -X PUT https://pixe.la/v1/users/a-know/graphs/test-graph/increment -H 'X-USER-TOKEN:thisissecret' -H 'Content-Length:0'
{"message":"Success.","isSuccess":true}```
