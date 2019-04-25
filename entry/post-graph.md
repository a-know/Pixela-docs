---
Title: POST - /v1/users/<username>/graphs
Date: 2019-04-23T21:44:17+09:00
URL: https://pixela-docs.hatenablog.com/entry/post-graph
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/17680117127076346928
---

### Description
Create a new pixelation graph definition.

### HTTP Method , API endpoint
<span class="badge badge-post">POST</span> `/v1/users/<username>/graphs`

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|


### Request Body

|Key|Type|Description|
|---|---|---|
|id|string|**[required]** It is an ID for identifying the pixelation graph.<br>Validation rule: ^[a-z][a-z0-9-]{1,16}|
|name|string|**[required]** It is the name of the pixelation graph.|
|unit|string|**[required]** It is a unit of the quantity recorded in the pixelation graph. Ex. commit, kilogram, calory.|
|type|string|**[required]** It is the type of quantity to be handled in the graph. Only int or float are supported.|
|color|string|**[required]** Defines the display color of the pixel in the pixelation graph.<br>`shibafu` (green), `momiji` (red), `sora` (blue), `ichou` (yellow), `ajisai` (purple) and `kuro` (black) are supported as color kind.|
|timezone|string|[optional] Specify the timezone for handling this graph as `Asia/Tokyo`. If not specified, it is treated as `UTC`.|
|selfSufficient|string|[optional] If SVG graph with this field `increment` or `decrement` is referenced, Pixel of this graph itself will be incremented or decremented.<br>It is suitable when you want to record the PVs on a web page or site simultaneously.<br>The specification of increment or decrement is the same as Increment a Pixel and Decrement a Pixel with webhook.<br>If not specified, it is treated as `none` .|

### Example

```sh
$ curl -X POST https://pixe.la/v1/users/a-know/graphs -H 'X-USER-TOKEN:thisissecret' -d '{"id":"test-graph","name":"graph-name","unit":"commit","type":"int","color":"shibafu","timezone":"Asia/Tokyo"}'
{"message":"Success.","isSuccess":true}
```
