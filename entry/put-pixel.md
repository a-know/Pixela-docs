---
Title: PUT - /v1/users/<username>/graphs/<graphID>/<yyyyMMdd>
Date: 2019-04-24T16:29:52+09:00
URL: https://pixela-docs.hatenablog.com/entry/put-pixel
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/17680117127076647587
---

### Description
Update the quantity already registered as a "Pixel". If target "Pixel" not exist, create a new "Pixel" and set quantity.

### HTTP Method , API endpoint
<span class="badge badge-put">PUT</span> `/v1/users/<username>/graphs/<graphID>/<yyyyMMdd>`

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|

### Request Body

|Key|Type|Description|
|---|---|---|
|quantity|string|[optional] Specify the quantity to be registered on the specified date.<br>Validation rule: int^\-?[0-9]+ float^\-?[0-9]+\.[0-9]+|
|optionalData|string|[optional] Additional information other than quantity. It is specified as JSON string.<br>The amount of this data must be less than 10 KB.|

### Example

```sh
$ curl -X PUT https://pixe.la/v1/users/a-know/graphs/test-graph/20180915 -H 'X-USER-TOKEN:thisissecret' -d '{"quantity":"7","optionalData":"{\"key\":\"value\"}"}'
{"message":"Success.","isSuccess":true}
```
