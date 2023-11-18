# Signup

```
/user/signup.php
```

### Parameters
| Name     | Type   | Description               |
|----------|--------|---------------------------|
| username | string | The username of the user. |
| password | string | The password of the user. |

### Description
This endpoint is used to sign up a user. After signing up, the API will return a `sid` which can be used to identify the user.

A new user begins with the `user` role. (ID 0)

*Warning!: The country section of the SID will be the country of the IP address that registered the account. And this __Cannot be changed!__*

### Returns
```json
HTTP 200 OK
{
	"data": {
		"sid": "string",
	},
	"error": null
}
```

```json
HTTP 400 Bad Request
{
	"data": null,
	"error": "string",
}
```