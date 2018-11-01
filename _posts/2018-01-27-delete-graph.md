---
category: Graph
resturi: '/v1/users/&lt;username&gt;/graphs/&lt;graphID&gt;'
title: 'Delete a graph'
type: 'DELETE'

layout: nil
---

Delete the predefined pixelation graph definition.

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|

### Example

```$ curl -X DELETE https://pixe.la/v1/users/a-know/graphs/test-graph -H 'X-USER-TOKEN:thisissecret'
{"message":"Success.","isSuccess":true}```
