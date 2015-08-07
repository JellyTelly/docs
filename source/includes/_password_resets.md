# Password Resets

## Send email with token

```ruby

```

```shell
curl -X POST -H "Cache-Control: no-cache" 'https://api.jellytelly.com/password_resets?email=test@email.com'
```

>The above command returns JSON structured like this:

```json

```

This endpoint sends an email to the address supplied, creating a reset token valid for 2 hours.


### HTTP Request

`POST /password_resets?email=<EMAIL> HTTP/1.1
Host: api.jellytelly.com
Cache-Control: no-cache`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
email | String | The email address to send reset token to | true


## Reset password

```ruby

```

```shell
curl -X PATCH -H "Cache-Control: no-cache" 'https://api.jellytelly.com/password_resets/abc?password=testuser&password_confirmation=testuser'
```


This endpoint resets the user password, validated by the reset token. This will logout the user requiring them to log back in.


### HTTP Request

`PATCH /password_resets/<TOKEN>?password=<PASSWORD>&password_confirmation=<PASSWORD_CONFIRMATION> HTTP/1.1
Host: api.jellytelly.com
Cache-Control: no-cache`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
token | String | The token from password reset email, this is a included automatically | true
password | String | The new password | true
password_confirmation | String | The new password confirmation, this should match the password | true
