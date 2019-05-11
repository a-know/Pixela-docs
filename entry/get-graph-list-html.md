---
Title: GET - /v1/users/<username>/graphs.html
Date: 2019-05-07T23:45:40+09:00
URL: https://docs.pixe.la/entry/get-graph-list-html
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/17680117127113526569
---

### Description
Displays graph list by detail in html format.


If you do not want to include a specific graph in the list displayed by using this function (if you want to make a specific graph private), [update the graph definition](https://docs.pixe.la/entry/put-graph) beforehand and set `true` to` isSecret` there is. This is a limited function for supporters. For details, Please refer to [https://github.com/a-know/Pixela/wiki/How-to-support-Pixela-by-Patreon-%EF%BC%8F-Use-Limited-Features:title] .


### HTTP Method , API endpoint
<span class="badge badge-get">GET</span> `/v1/users/<username>/graphs.html`

### Example

```sh
$ open https://pixe.la/v1/users/a-know/graphs.html
```
