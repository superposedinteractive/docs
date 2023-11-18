# Friend request accept

```
/social/accept.php
```

*A valid user token is required.*

### Parameters
| Name | Type   | Description                                                   |
|------|--------|---------------------------------------------------------------|
| sid  | string | The SID of the user you want to accept a friend request from. |

### Description
This endpoint is used to accept a friend request. On success, the API will return `200 OK` with no data.

In case of a friend request not existing, the API will return a `404 Not Found` HTTP status code along with the corresponding error message.

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