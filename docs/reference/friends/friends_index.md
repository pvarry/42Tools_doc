---
bodyclass: docs
layout: docs
headline: Friends - GET
sidenav: doc-side-tutorial-nav.html
type: markdown
---
<p class="lead">GET on Friends</p>

# GET /friends

Returns friends of the logged user.

> Authentification requiered

## Endpoint definition

`GET /v1/friends`

## Parameters

| Parameter | Description | Data Type |
|-----------|------|-----|-----------|
| per_page | *Optional*. The number of item per page. Default is 30. | integer |
| page | *Optional*. Index of the page. Default is 30. | integer |

## Sample request

```
curl -I -X GET "http://api.42.tools/v1/friends"
```

## Sample response

```json
[
	{
		"id": 11857,
		"login": "skerkour",
		"group_ids": [
			1
		]
	},
	{
		"id": 11814,
		"login": "eeugene",
		"group_ids": []
	},
	{
		"id": 21219,
		"login": "imurawsk",
		"group_ids": []
	},
	{
		"id": 28889,
		"login": "jrobinea",
		"group_ids": []
	}
]
```

The following table describes each item in the response.

|Response item | Description |
|----------|------------|
| **id** | The id of the friend from 42 database. |
| **login** | The login of the friend. |
| **group_ids** | A list of ids. This list represent the groups (or labels) of this friend. |

## Error and status codes

The following table lists the status and error codes related to this request.

| Status code | Meaning |
|--------|----------|
| 200 | Successful response |
| 400 | Bad request -- one or more of the parameters was rejected. |
| 401 | Unauthorized -- a valid authorisation must be specified. |
