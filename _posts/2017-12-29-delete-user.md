---
category: User
resturi: '/v1/users/&lt;username&gt;'
title: 'Delete a user'
type: 'DELETE'

layout: nil
---

Deletes the specified registered user.

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|


### Example

```$ curl -X DELETE https://pixe.la/v1/users/a-know -H 'X-USER-TOKEN:thisissecret'
{"message":"Success.","isSuccess":true}```
