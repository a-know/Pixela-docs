---
Title: POST - /v1/users/<username>/graphs/<graphID>
Date: 2019-04-24T16:26:13+09:00
URL: https://docs.pixe.la/entry/post-pixel
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/17680117127076646122
---

### Description
It records the quantity of the specified date as a "Pixel".

### HTTP Method , API endpoint
<span class="badge badge-post">POST</span> `/v1/users/<username>/graphs/<graphID>`

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

```sh
$ curl -X POST https://pixe.la/v1/users/a-know/graphs/test-graph -H 'X-USER-TOKEN:thisissecret' -d '{"date":"20180915","quantity":"5","optionalData":"{\"key\":\"value\"}"}'
{"message":"Success.","isSuccess":true}
```
