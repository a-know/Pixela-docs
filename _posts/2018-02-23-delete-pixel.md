---
category: Pixel
resturi: '/v1/users/&lt;username&gt;/graphs/&lt;graphID&gt;/&lt;yyyyMMdd&gt;'
title: 'Delete a Pixel'
type: 'DELETE'

layout: nil
---

Delete the registered "Pixel".

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|

### Example

```$ curl -X DELETE https://pixe.la/v1/users/a-know/graphs/test-graph/20180915 -H 'X-USER-TOKEN:thisissecret'
{"message":"Success.","isSuccess":true}```
