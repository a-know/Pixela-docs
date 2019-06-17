---
Title: GET - /v1/users/<username>/graphs/<graphID>.html
Date: 2019-04-24T07:03:03+09:00
URL: https://docs.pixe.la/entry/get-graph-html
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/17680117127076486017
---

### Description
Displays the details of the graph in html format.

### HTTP Method , API endpoint
<span class="badge badge-get">GET</span> `/v1/users/<username>/graphs/<graphID>.html`

### Query Parameter

|Key|type|Description|
|---|---|---|
|mode|string|[optional] You can get a very simple html response by specifying `simple` or `simple-short` with this parameter.<br>Useful in combination with iframe tags.|

### Example

```sh
$ open https://pixe.la/v1/users/a-know/graphs/test-graph.html
```


```sh
$ open https://pixe.la/v1/users/a-know/graphs/test-graph.html?mode=simple
```
