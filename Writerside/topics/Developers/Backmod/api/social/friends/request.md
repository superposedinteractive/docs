# Friend Request

```
/social/request.php
```

*A valid user token is required.*

### Parameters
| Name | Type   | Description                                     |
|------|--------|-------------------------------------------------|
| sid  | string | The SID of the user you want to friend request. |

### Description
This endpoint is used to send a friend request to the user. On success, the API will return `200 OK` with no data.

In case of an friendship status existing, the API will return a `208 Already Reported` HTTP status code along with the corresponding error message.

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