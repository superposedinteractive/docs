# Sign in

```
/user/signin.php
```

### Parameters
| Name     | Type   | Description               |
|----------|--------|---------------------------|
| username | string | The username of the user. |
| password | string | The password of the user. |

### Description
This endpoint is used to sign in to a user. After signing in, the API will return a `token` which can be used to do other API calls.

The token is valid for 7 days and extended with each use. The token can be entirely reset by signing in again.

### Returns
```json
HTTP 200 OK
{
	"data": {
		"token": "string",
		"note": "This token is valid for 7 days, or until you sign in again. Obviously never give this token to anyone."
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