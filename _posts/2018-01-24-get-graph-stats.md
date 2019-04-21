---
category: Graph
resturi: '/v1/users/&lt;username&gt;/graphs/&lt;graphID&gt;/stats'
title: 'Get a graph stats'
type: 'GET'

layout: nil
---

Based on the registered information, get various statistics.


### Example

```$ curl -X GET https://pixe.la/v1/users/a-know/graphs/test-graph/stats
{"totalPixelsCount":4,"maxQuantity":7,"minQuantity":4,"totalQuantity":25,"avgQuantity":6.25,"todaysQuantity":3}```
