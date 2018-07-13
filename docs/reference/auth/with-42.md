---
bodyclass: docs
layout: docs
headline: Authentication
sidenav: doc-side-tutorial-nav.html
type: markdown
---
<p class="lead">POST</p>

# POST /auth

Create a Bearer Token with a 42 API token, this token will be used to verify authenticity of the user and generate a 42Tools API token. The token will be used twice, 1st to verify witch app is used to generate this token, and the second to know the ressource owner (the user), this information will be used to manage private data like friends.

## Endpoint definition

`POST /v1/auth`

## Parameters

| Parameter | Description | Data Type |
|-----------|------|-----|-----------|
| access_token | Use a 42's API token. | 42 token |


## Sample request

```
curl -I -X POST "https://api.42.tools/v1/auth?access_token=xxxx"
```

## Sample response

```json
{
    "access_token": "xxxx"
}
```

The following table describes each item in the response.

|Response item | Description |
|----------|------------|
| **access_token** | new 42 Tools token. |

## Error and status codes

The following table lists the status and error codes related to this request.

| Status code | Meaning |
|--------|----------|
| 200 | Successful response |
| 400 | Bad request -- one or more of the parameters was rejected. |
| 403 | Forbidden -- a valid 42 token must be specified. |
