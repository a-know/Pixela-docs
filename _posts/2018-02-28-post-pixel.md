---
category: Pixel
resturi: '/v1/users/&lt;username&gt;/graphs/&lt;graphID&gt;'
title: 'Post a Pixel'
type: 'POST'

layout: nil
---

It records the quantity of the specified date as a "Pixel".

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|

### Request Body

|Key|Type|Description|
|---|---|---|
|date|string|**[required]** The date on which the quantity is to be recorded. It is specified in yyyyMMdd format.|
|quantity|string|**[required]** Specify the quantity to be registered on the specified date.<br>Validation rule: int^\-?[0-9]+ float^\-?[0-9]+\.[0-9]+|
|optionalData|string|[optional] Additional information other than quantity. It is specified as JSON string.<br>The amount of this data must be less than 10 KB.|

### Example

```$ curl -X POST https://pixe.la/v1/users/a-know/graphs/test-graph -H 'X-USER-TOKEN:thisissecret' -d '{"date":"20180915","quantity":"5","optionalData":"{\"key\":\"value\"}"}'
{"message":"Success.","isSuccess":true}```
