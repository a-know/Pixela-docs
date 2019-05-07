---
Title: POST - /v1/users
Date: 2019-04-23T20:19:57+09:00
URL: https://docs.pixe.la/entry/post-user
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/17680117127076310307
---

### Description
Create a new Pixela user.

### HTTP Method , API endpoint
<span class="badge badge-post">POST</span> `/v1/users`

### Request Body

|Key|Type|Description|
|---|---|---|
|token|string|**[required]** A token string used to authenticate as a user to be created. The token string is hashed and saved.<br>Validation rule: [ -~]{8,128}|
|username|string|**[required]** User name for this service.<br>Validation rule: [a-z][a-z0-9-]{1,32}|
|agreeTermsOfService|string|**[required]** Specify yes or no whether you agree to the terms of service.<br>Please see: [Terms of service - Japanese version](https://github.com/a-know/Pixela/wiki/%E5%88%A9%E7%94%A8%E8%A6%8F%E7%B4%84%EF%BC%88Terms-of-Service-Japanese-Version%EF%BC%89) / [Terms of service - English version](https://github.com/a-know/Pixela/wiki/Terms-of-Service)|
|notMinor|string|**[required]** Specify yes or no as to whether you are not a minor or if you are a minor and you have the parental consent of using this service.|
|thanksCode|string|[optional] Set `thanks-code` . If it is a valid `thanks-code`, some limited features will be available. For details, please check [How to support Pixela by Patreon ／ Use Limited Features](https://github.com/a-know/Pixela/wiki/How-to-support-Pixela-by-Patreon-%EF%BC%8F-Use-Limited-Features).|


### Example

```sh
$ curl -X POST https://pixe.la/v1/users -d '{"token":"thisissecret", "username":"a-know", "agreeTermsOfService":"yes", "notMinor":"yes", "thanksCode":"ThisIsThanksCode"}'
{"message":"Success.","isSuccess":true}
```
