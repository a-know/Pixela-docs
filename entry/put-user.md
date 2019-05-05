---
Title: PUT - /v1/users/<username>
Date: 2019-04-23T21:36:43+09:00
URL: https://docs.pixe.la/entry/put-user
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/17680117127076343620
---

### Description
Updates the authentication token for the specified user.

### HTTP Method , API endpoint
<span class="badge badge-put">PUT</span> `/v1/users/<username>`

### Request Header

|Key|Description|
|---|---|
|X-USER-TOKEN|**[required]** It is the authentication token specified at the time of user registration.|


### Request Body

|Key|Type|Description|
|---|---|---|
|newToken|string|**[required]** It is a new authentication token. The token string is hashed and saved.<br>Validation rule: [ -~]{8,128}|
|thanksCode|string|[optional] Set `thanks-code` . If it is a valid `thanks-code`, some limited features will be available. For details, please check [How to support Pixela by Patreon ／ Use Limited Features](https://github.com/a-know/Pixela/wiki/How-to-support-Pixela-by-Patreon-%EF%BC%8F-Use-Limited-Features).|

### Example

```sh
$ curl -X PUT https://pixe.la/v1/users/a-know -H 'X-USER-TOKEN:thisissecret' -d '{"newToken":"thisissecret","thanksCode":"ThisIsThanksCode"}'
{"message":"Success.","isSuccess":true}
```
