# User Block

```
/social/block.php
```

*A valid user token is required.*

### Parameters
| Name | Type   | Description                            |
|------|--------|----------------------------------------|
| sid  | string | The SID of the user you want to block. |

### Description
This endpoint is used to block all social interaction with an user. On success, the API will return `200 OK` with no data.

In case the user is already blocked, the API will return a `208 Already Reported` HTTP status code.

### Returns
```json
HTTP 200 OK
{
	"data": null,
	"error": null
}
```

```json
HTTP 208 Already Reported
{
	"data": null,
	"error": "string"
}
```