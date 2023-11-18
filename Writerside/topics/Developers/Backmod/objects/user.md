# The User Object
The `user` object contains general information pertaining to registered users.
Retrieving this object requires the user's `SID`. The structure
of this object is as follows:
```json
{
	"username": "Player",                              // string
	"avatar_url": "https://cdn.dzejmod.tk/avatar/...", // string
	"register_time": 0,                                // UNIX Timestamp | int
	"last_seen_time": 0,                               // UNIX Timestamp | int
	"role": 0,                                         // User role | int
}
```

In the JSON structure provided:
- `username` denotes the user's designated name, represented as a string.
- `avatar_url` indicates the URL of the user's avatar, conveyed as a string.
- `register_time` signifies the registration date in UNIX Timestamp format integer.
- `last_seen_time` indicates the most recent login date in UNIX Timestamp format integer.
- `role` portrays the role attributed to the user, conveyed as an integer.

### The `SID` Structure
The `SID` Structure is a way of representing an user using a
combination of alphanumeric characters. It's made up of three parts:
USER, REGION, and SALT, separated by colons.

1. **USER**: This part is always represented as "USER" and remains constant.
It's like a fixed label that indicates the type of entity or object being identified.
2. **REGION**: This part represents the region and follows the ISO 3166-1 alpha-2 country codes.
ISO 3166-1 alpha-2 codes are two-letter country codes that uniquely identify countries or regions.
For example, "US" stands for the United States, "CA" stands for Canada, and so on.
3. **SALT**: This part is a variable alphanumeric string of characters.
The term "salt" usually refers to random data that is used to modify the input of a hash function,
adding randomness and making the hash more secure. In this case, it's part of the
identifier and could be any combination of characters.

So, when you put all these parts together, a `SID` would look like this:

```
USER:REGION:SALT
```

For example, let's say we have a user from the United States,
and his `SID` is "USER:US:AB12CD". Here's how the parts break down:

- **USER**: USER
- **REGION**: US (United States)
- **SALT**: AB12CD

Putting it all together: USER:US:AB12CD

This `SID` uniquely identifies an user from the United States
with the specific salt "AB12CD".

### Types of `role`s that users can have
Users are classified into different roles, each with specific
permissions and responsibilities. Below are the various user
roles along with their associated attributes:

| Role         | Description                                                                                                                                                       | ID  |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
| `user`       | Regular users holding standard permissions.                                                                                                                       | 0   |
| `nuisance`   | Users who have faced numerous reports or have been manually designated as such by a moderator. These users are restricted from uploading to the addon repository. | 1   |
| `developer`  | Trusted developers with elevated privileges; they can bypass dzejLabs (purgatory) and directly upload to the public repository.                                   | 2   |
| `superposed` | superposed employees enjoying extensive administrative tools access, LOL.                                                                                         | 999 |