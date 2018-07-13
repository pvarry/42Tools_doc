---
bodyclass: docs
layout: docs
headline: Friends - POST
sidenav: doc-side-tutorial-nav.html
type: markdown
---
<p class="lead">POST</p>

# POST /friends

Add a user in the friends list.

> Authentification requiered

## Endpoint definition

`POST /v1/friends`

## Parameters

| Parameter | Description | Data Type |
|-----------|------|-----|-----------|
| user_id | The user to add. | integer. 42 user ID|


## Sample request

```
curl -I -X POST "http://api.42.tools/v1/friends?user_id=11058"
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
