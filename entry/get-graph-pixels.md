---
Title: GET - /v1/users/<username>/graphs/<graphID>/pixels
Date: 2019-04-24T07:06:34+09:00
URL: https://pixela-docs.hatenablog.com/entry/get-graph-pixels
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/17680117127076486750
---

### Description
Get a Date list of Pixel registered in the graph specified by graphID.<br>
You can specify a period with from and to parameters.<br>

- If you do not specify both `from` and` to`;
    - You will get a list of 365 days ago from today.
- If you specify `from` only;
    - You will get a list of 365 days from `from` date.
- If you specify `to` only;
    - You will get a list of 365 days ago from `to` date.
- If you specify both `from` and` to`;
    - You will get a list you specify.
    - You can not specify a period greater than 365 days.

### HTTP Method , API endpoint
<span class="badge badge-get">GET</span> `/v1/users/<username>/graphs/<graphID>/pixels`

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|


### Query Parameter

|Key|Type|Description|
|---|---|---|
|from|string|[optional] Specify the start position of the period.|
|to|string|[optional] Specify the end position of the period.|

### Example

```sh
$ curl -X GET https://pixe.la/v1/users/a-know/graphs/test-graph/pixels?from=20180101&to=20181231 -H 'X-USER-TOKEN:thisissecret'
{"pixels":["20180101","20180331","20180402","20180505","20181204"]}
```
