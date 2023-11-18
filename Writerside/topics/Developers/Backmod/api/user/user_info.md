# User info

```
/user/info.php
```

*A valid user token is required.*

### Parameters
| Name | Type   | Description                             |
|------|--------|-----------------------------------------|
| sid  | string | The SID of the user you want to lookup. |

### Description
This endpoint is used to fetch info of an user. The API will return:

| Name           | Type   | Description                                     |
|----------------|--------|-------------------------------------------------|
| username       | string | The username.                                   |
| avatar_url     | string | The URL of the users avatar.                    |
| last_seen_time | int    | The UNIX timestamp when the user was last seen. |
| register_time  | int    | The UNIX timestamp when the user registered.    |
| role           | int    | The user role.                                  |

### Returns
```json
HTTP 200 OK
{
	"data": {
		"username": "string",
		"avatar_url": "string",
		"last_seen_time": int,
		"register_time": int,
		"role": int,
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