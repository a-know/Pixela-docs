---
Title: GET - /v1/users/<username>/graphs/<graphID>/stats
Date: 2019-04-24T07:07:58+09:00
URL: https://pixela-docs.hatenablog.com/entry/get-graph-stats
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/17680117127076487018
---

### Description
Based on the registered information, get various statistics.

### HTTP Method , API endpoint
<span class="badge badge-get">GET</span> `/v1/users/<username>/graphs/<graphID>/stats`

### Example

```sh
$ curl -X GET https://pixe.la/v1/users/a-know/graphs/test-graph/stats
{"totalPixelsCount":4,"maxQuantity":7,"minQuantity":4,"totalQuantity":25,"avgQuantity":6.25,"todaysQuantity":3}
```
