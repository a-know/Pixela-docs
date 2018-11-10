---
category: Graph
resturi: '/v1/users/&lt;username&gt;/graphs'
title: 'Create a graph'
type: 'POST'

layout: nil
---

Create a new pixelation graph definition.

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

### Example

```$ curl -X POST https://pixe.la/v1/users/a-know/graphs -H 'X-USER-TOKEN:thisissecret' -d '{"id":"test-graph","name":"graph-name","unit":"commit","type":"int","color":"shibafu","timezone":"Asia/Tokyo"}'
{"message":"Success.","isSuccess":true}```
