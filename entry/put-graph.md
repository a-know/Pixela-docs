---
Title: PUT - /v1/users/<username>/graphs/<graphID>
Date: 2019-04-24T06:58:45+09:00
URL: https://docs.pixe.la/entry/put-graph
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/17680117127076484572
---

### Description
Update predefined pixelation graph definitions.<br>The items that can be updated are limited as compared with the pixelation graph definition creation.

### HTTP Method , API endpoint
<span class="badge badge-put">PUT</span> `/v1/users/<username>/graphs/<graphID>`

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|


### Request Body

|Key|Type|Description|
|---|---|---|
|name|string|[optional] It is the name of the pixelation graph.|
|unit|string|[optional] It is a unit of the quantity recorded in the pixelation graph. Ex. commit, kilogram, calory.|
|color|string|[optional] Defines the display color of the pixel in the pixelation graph.<br>`shibafu` (green), `momiji` (red), `sora` (blue), `ichou` (yellow), `ajisai` (purple) and `kuro` (black) are supported as color kind.|
|timezone|string|[optional] Specify the timezone for handling this graph as `Asia/Tokyo`. If not specified, it is treated as `UTC`.|
|purgeCacheURLs|array[string]|[optional] This is an advanced option.<br>Specify the URL to send the purge request to purge the cache when the graph is updated.<br>For example, in GitHub, since all images referenced from GitHub are cached, it is necessary to purge the cache every time the Pixeleation graph is changed.<br>Even with the same Pixelation graph, different cache URLs are generated when referring from multiple places, you can specify up to 5 URLs.|
|selfSufficient|string|[optional] If SVG graph with this field `increment` or `decrement` is referenced, Pixel of this graph itself will be incremented or decremented.<br>It is suitable when you want to record the PVs on a web page or site simultaneously.<br>The specification of increment or decrement is the same as Increment a Pixel and Decrement a Pixel with webhook.<br>If not specified, it is treated as `none` .|

### Example

```sh
$ curl -X PUT https://pixe.la/v1/users/a-know/graphs/test-graph -H 'X-USER-TOKEN:thisissecret' -d '{"name":"graph-name","unit":"commit","color":"shibafu","timezone":"Asia/Tokyo","purgeCacheURLs":["https://camo.githubusercontent.com/xxx/xxxx"]}'
{"message":"Success.","isSuccess":true}
```
