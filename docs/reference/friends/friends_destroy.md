---
bodyclass: docs
layout: docs
headline: Friends - DELETE
sidenav: doc-side-tutorial-nav.html
type: markdown
---
<p class="lead">DELETE on Friend</p>

# DELETE /friends/:id

Add a user in the friends list.

> Authentification requiered

## Endpoint definition

`DELETE /v1/friends/:id`

`:id` refers to the ID of the requested data. Use a 42 user ID.


## Sample request

```
curl -I -X DELETE "https://api.42.tools/v1/friends/11058"
```

## Error and status codes

The following table lists the status and error codes related to this request.

| Status code | Meaning |
|--------|----------|
| 204 | No Content - successful operation |
| 400 | Bad request -- one or more of the parameters was rejected. |
| 401 | Unauthorized -- a valid authorisation must be specified. |
