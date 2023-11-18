# Friend List

```
/social/list.php
```

*A valid user token is required.*

### Parameters
#### No parameters

### Description
This endpoint is used to fetch the friends of the user. The API will return:

| Name   | Type | Description                   |
|--------|------|-------------------------------|
| sid    | user | The user object.              |
| status | int  | The status of the friendship. |

### Status Codes
The API may return different status codes based on the state of the friend request. Here's what each status code means:

| Status Code | Description                                                                                                              |
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| `0`         | Friend request already sent. If you've already sent a friend request to this user, the API will return this status code. |
| `1`         | Already friends. If you're already friends with this user, the API will return this status code.                         |
| `2`         | Blocked. If the user has blocked you, the API will return this status code.                                              |

### Returns
```json
HTTP 200 OK
{
	"data": {
		"sid": {user},
		"sid": {user},
		...
	},
	"error": null
}
```

```json
HTTP 400 Bad Request
{
	"data": null,
	"error": "string"
}
```