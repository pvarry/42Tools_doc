---
bodyclass: docs
layout: docs
headline: Friends - GET
sidenav: doc-side-tutorial-nav.html
type: markdown
---
<p class="lead">GET a specific Friend</p>

# GET /friends/:id

Returns a specific friend, olso used to know if someone is added as friend

> Authentification requiered

## Endpoint definition

`/v1/friends/:id`

`:id`
 : refers to the ID of the requested data. Use a 42 user ID.

## Sample request

```
curl -I -X GET "http://api.42.tools/v1/friends/11058"
```

## Sample response

```json
{
    "id": 11058,
    "login": "jpucelle",
    "added_at": "2018-01-03T13:28:42.309Z",
    "groups": [1,2]
}
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
| 404 | Not Found -- this user is not added as friends of the logged user |
