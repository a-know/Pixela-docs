---
Title: GET - /v1/users/<username>/graphs/<graphID>
Date: 2019-04-24T06:56:21+09:00
URL: https://pixela-docs.hatenablog.com/entry/get-svg
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/17680117127076484068
---

### Description
Based on the registered information, express the graph in SVG format diagram.

### HTTP Method , API endpoint
<span class="badge badge-get">GET</span> `/v1/users/<username>/graphs/<graphID>`

### Query Parameter

|Key|Description|
|---|---|
|date|string|[optional] If you specify it in yyyyMMdd format, will create a pixelation graph dating back to the past with that day as the start date.<br>If this parameter is not specified, the current date and time will be the start date.<br>(it is used `timezone` setting if Graph's `timezone` is specified, if not specified, calculates it in `UTC`)|
|mode|string|[optional] Specify the graph display mode.<br>Supported modes are `short` (for displaying only about 90 days) and `line` .|


### Example

```sh
$ curl -X GET https://pixe.la/v1/users/a-know/graphs/test-graph?date=20180331&mode=short
<svg xmlns="http://www.w3.org/2000/svg" width="220" height="135" ...
```
