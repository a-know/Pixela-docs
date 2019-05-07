---
Title: API Index
Date: 2019-04-23T19:08:24+09:00
URL: https://docs.pixe.la/entry/api-index
EditURL: https://blog.hatena.ne.jp/a-know/pixela-docs.hatenablog.com/atom/entry/17680117127072086112
---

## User
#### [<span class="badge badge-post">POST</span> `/v1/users` - Create a user](https://pixela-docs.hatenablog.com/entry/post-user)


#### [<span class="badge badge-put">PUT</span> `/v1/users/<username>` - Update a user](https://pixela-docs.hatenablog.com/entry/put-user)


#### [<span class="badge badge-delete">DELETE</span> `/v1/users/<username>` - Delete a user](https://pixela-docs.hatenablog.com/entry/delete-user)


<hr>


## Graph
#### [<span class="badge badge-post">POST</span> `/v1/users/<username>/graphs` - Create a graph](https://pixela-docs.hatenablog.com/entry/post-graph)


#### [<span class="badge badge-get">GET</span> `/v1/users/<username>/graphs` - Get graph definitions](https://pixela-docs.hatenablog.com/entry/get-graph)


#### [<span class="badge badge-get">GET</span> `/v1/users/<username>/graphs/<graphID>` - Get a graph SVG](https://pixela-docs.hatenablog.com/entry/get-svg)


#### [<span class="badge badge-put">PUT</span> `/v1/users/<username>/graphs/<graphID>` - Update a graph](https://pixela-docs.hatenablog.com/entry/put-graph)


#### [<span class="badge badge-delete">DELETE</span> `/v1/users/<username>/graphs/<graphID>` - Delete a graph](https://pixela-docs.hatenablog.com/entry/delete-graph)


#### [<span class="badge badge-get">GET</span> `/v1/users/<username>/graphs/<graphID>.html` - View a graph detail](https://pixela-docs.hatenablog.com/entry/get-graph-html)


#### [<span class="badge badge-get">GET</span> `/v1/users/<username>/graphs.html` - View graph list by detail](https://pixela-docs.hatenablog.com/entry/get-graph-list-html)


#### [<span class="badge badge-get">GET</span> `/v1/users/<username>/graphs/<graphID>/pixels` - Get graph pixels list](https://pixela-docs.hatenablog.com/entry/get-graph-pixels)


#### [<span class="badge badge-get">GET</span> `/v1/users/<username>/graphs/<graphID>/stats` - Get a graph stats](https://pixela-docs.hatenablog.com/entry/get-graph-stats)


<hr>


## Pixel
#### [<span class="badge badge-post">POST</span> `/v1/users/<username>/graphs/<graphID>` - Post a pixel](https://pixela-docs.hatenablog.com/entry/post-pixel)


#### [<span class="badge badge-get">GET</span> `/v1/users/<username>/graphs/<graphID>/<yyyyMMdd>` - Get a pixel](https://pixela-docs.hatenablog.com/entry/get-pixel)


#### [<span class="badge badge-put">PUT</span> `/v1/users/<username>/graphs/<graphID>/<yyyyMMdd>` - Update a pixel](https://pixela-docs.hatenablog.com/entry/put-pixel)


#### [<span class="badge badge-put">PUT</span> `/v1/users/<username>/graphs/<graphID>/increment` - Increment a pixel](https://pixela-docs.hatenablog.com/entry/increment-pixel)


#### [<span class="badge badge-put">PUT</span> `/v1/users/<username>/graphs/<graphID>/decrement` - Decrement a pixel](https://pixela-docs.hatenablog.com/entry/decrement-pixel)


#### [<span class="badge badge-delete">DELETE</span> `/v1/users/<username>/graphs/<graphID>/<yyyyMMdd>` - Delete a pixel](https://pixela-docs.hatenablog.com/entry/delete-pixel)


<hr>


## Webhook
#### [<span class="badge badge-post">POST</span> `/v1/users/<username>/webhooks` - Create a webhook](https://pixela-docs.hatenablog.com/entry/post-webhook)


#### [<span class="badge badge-get">GET</span> `/v1/users/<username>/webhooks` - Get webhooks](https://pixela-docs.hatenablog.com/entry/get-webhook)


#### [<span class="badge badge-post">POST</span> `/v1/users/<username>/webhooks/<webhookHash>` - Invoke a webhook](https://pixela-docs.hatenablog.com/entry/invoke-webhook)


#### [<span class="badge badge-delete">DELETE</span> `/v1/users/<username>/webhooks/<webhookHash>` - Delete a webhook](https://pixela-docs.hatenablog.com/entry/delete-webhook)


<hr>
