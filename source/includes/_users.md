# Users

## Signup

```ruby
u = User.save(user[email]: email, user[password]: password, user[password_confirmation]: password_confirmation)
```

```shell
curl -X POST -H "Cache-Control: no-cache" 'http://api.jellytelly.com/signup?user[email]=test@email.com&user[password]=testuser&user[password_confirmation]=testuser&user[username]=test@email.com'
```

>The above command returns JSON structured like this:

```json
{
  "user_info": {
    "status": "Active",
    "id": 12,
    "email": "test@email.com",
    "crypted_password": "$2a$10$s0sPePDL.4LCmI8EOwfe1u5IWCfGgbtZxPJEa0evKHbeSbNIj32d6",
    "salt": "tHyVeKFR5UTmycsaqzKo",
    "created_at": "2015-08-04T14:18:32.580-05:00",
    "updated_at": "2015-08-04T14:18:32.580-05:00",
    "reset_password_token": null,
    "reset_password_token_expires_at": null,
    "reset_password_email_sent_at": null,
    "failed_logins_count": 0,
    "lock_expires_at": null,
    "unlock_token": null,
    "last_login_at": null,
    "last_logout_at": null,
    "last_activity_at": null,
    "last_login_from_ip_address": null,
    "auth_token": "f9bdb8944a6c40ab81b02089dda70142",
    "role": "user",
    "active_episode": null,
    "first_name": null,
    "last_name": null,
    "username": "test@email.com",
    "subscriber_account_id": null,
    "subscription_source": "Web"
  }
}
```

This endpoint creates a user account, with a role of user. This user will not be able to perform any additional actions until they create a subscription.

<aside class="warning">If you're not using an administrator API key, note that some users will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`POST https://api.jellytelly.com/signup?user[email]=email&user[password]=password&user[password_confirmation]=password_confirmation&user[username]=email<ID>`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
user | Hash | The user hash object, all parameters must be passed in the user hash | true
user[email] | String | Email of the user | true
user[password] | String | User password, minimum length: 6 chars | true
user[password_confirmation] | String | User password_confirmation, must match password | true
user[username] | String | Username for all new users is their email | true

## Login

```ruby
u = User.login(email: email, password: password)
```

```shell
curl -X POST -H "Cache-Control: no-cache" 'http://apidev.jellytelly.com/login?email=test@email.com&password=testuser'
```

> The above command returns JSON structured like this:

```json
{
  "user_info": {
    "id": 1,
    "email": "test@email.com",
    "crypted_password": "$2a$10$Q7BmoWFNDEgCilACYhPK4u8ygbV4X8cYlNhn4bjVLOv2g9h1D1xBe",
    "salt": "iiqSBzNWDycyJeuzBqbS",
    "created_at": "2015-07-25T02:11:48.314-05:00",
    "updated_at": "2015-08-04T14:49:09.161-05:00",
    "reset_password_token": null,
    "reset_password_token_expires_at": null,
    "reset_password_email_sent_at": null,
    "failed_logins_count": 0,
    "lock_expires_at": null,
    "unlock_token": null,
    "last_login_at": "2015-08-04T14:49:09.157-05:00",
    "last_logout_at": null,
    "last_activity_at": "2015-08-04T13:56:40.341-05:00",
    "last_login_from_ip_address": "127.0.0.1",
    "status": "Active",
    "auth_token": "ef07550a2ee14d8d8f9b54ec8e6f95f2",
    "role": "subscriber",
    "active_episode": "dxeG41dTrpdi41J069c1syLsLsUQyk2U",
    "first_name": "Test",
    "last_name": "User",
    "username": "test@email.com",
    "subscriber_account_id": "1",
    "subscription_source": "Web"
  }
}
```

This endpoint validates and logs a user into the system; returning user specific information. This is a session action.

### HTTP Request

`POST https://api.jellytelly.com/login?email=<EMAIL>&password=<PASSWORD>`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
EMAIL | String | The email of the user | true
PASSWORD | String | The password of the user | true

## Logout

```ruby
User.logout
```

```shell
curl -X DELETE -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://apidev.jellytelly.com/logout'
```

This method deletes the user session, resets the auth_token to an unknown value, and returns a 204. This is a session action.

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`DELETE /logout HTTP/1.1
Host: apidev.jellytelly.com
Authorization: Token token="auth_token"`


## Find

```ruby
u = User.find(1)
or
u = User.find('test@email.com')
```

```shell
curl -X GET -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/users/1'
or
curl -X GET -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/users/test@email.com'
```

> The above command returns JSON structured like this:

```json
{
  "user_info": {
    "subscription_source": "Web",
    "subscriber_account_id": "1",
    "id": 1,
    "email": "test@email.com",
    "crypted_password": "$2a$10$Q7BmoWFNDEgCilACYhPK4u8ygbV4X8cYlNhn4bjVLOv2g9h1D1xBe",
    "salt": "iiqSBzNWDycyJeuzBqbS",
    "created_at": "2015-07-25T02:11:48.314-05:00",
    "updated_at": "2015-08-03T15:19:19.969-05:00",
    "reset_password_token": null,
    "reset_password_token_expires_at": null,
    "reset_password_email_sent_at": null,
    "failed_logins_count": 0,
    "lock_expires_at": null,
    "unlock_token": null,
    "last_login_at": "2015-08-03T15:19:19.964-05:00",
    "last_logout_at": null,
    "last_activity_at": "2015-08-03T15:19:31.557-05:00",
    "last_login_from_ip_address": "127.0.0.1",
    "status": "Active",
    "auth_token": "c94333418ffb4e2fba4dd46abf48c5bf",
    "role": "subscriber",
    "active_episode": "dxeG41dTrpdi41J069c1syLsLsUQyk2U",
    "first_name": "Test",
    "last_name": "User",
    "username": "test@email.com"
  },
  "billing_info": {
    "id": "1",
    "object": "customer",
    "created": 1437808306,
    "livemode": false,
    "description": null,
    "email": "test@email.com",
    "delinquent": false,
    "metadata": {},
    "subscriptions": {
      "object": "list",
      "total_count": 1,
      "has_more": false,
      "url": "/v1/customers/1/subscriptions",
      "data": [
        {
          "id": "sub_6fiIsrRmV7tC9C",
          "plan": {
            "id": "JTA",
            "interval": "year",
            "name": "JellyTelly Annual Subscription",
            "created": 1435255142,
            "amount": 4000,
            "currency": "usd",
            "object": "plan",
            "livemode": false,
            "interval_count": 1,
            "trial_period_days": 7,
            "metadata": {},
            "statement_descriptor": "jellytellysubscription"
          },
          "object": "subscription",
          "start": 1437808478,
          "status": "active",
          "customer": "1",
          "cancel_at_period_end": false,
          "current_period_start": 1438413278,
          "current_period_end": 1470035678,
          "ended_at": null,
          "trial_start": 1437808478,
          "trial_end": 1438413278,
          "canceled_at": null,
          "quantity": 1,
          "application_fee_percent": null,
          "discount": {
            "coupon": {
              "id": "10OFF",
              "created": 1435255193,
              "percent_off": 10,
              "amount_off": null,
              "currency": null,
              "object": "coupon",
              "livemode": false,
              "duration": "forever",
              "redeem_by": null,
              "max_redemptions": null,
              "times_redeemed": 5,
              "duration_in_months": null,
              "valid": true,
              "metadata": {}
            },
            "start": 1437809621,
            "object": "discount",
            "customer": "1",
            "subscription": "sub_6fiIsrRmV7tC9C",
            "end": null
          },
          "tax_percent": null,
          "metadata": {}
        }
      ]
    },
    "discount": null,
    "account_balance": 0,
    "currency": "usd",
    "sources": {
      "object": "list",
      "total_count": 1,
      "has_more": false,
      "url": "/v1/customers/1/sources",
      "data": [
        {
          "id": "card_16SMrWJDs1f4mwxyWsxeTeHV",
          "object": "card",
          "last4": "4242",
          "brand": "Visa",
          "funding": "credit",
          "exp_month": 7,
          "exp_year": 2016,
          "fingerprint": "ZKGeE06WDAjRNkph",
          "country": "US",
          "name": null,
          "address_line1": null,
          "address_line2": null,
          "address_city": null,
          "address_state": null,
          "address_zip": null,
          "address_country": null,
          "cvc_check": "pass",
          "address_line1_check": null,
          "address_zip_check": null,
          "tokenization_method": null,
          "dynamic_last4": null,
          "metadata": {},
          "customer": "1"
        }
      ]
    },
    "default_source": "card_16SMrWJDs1f4mwxyWsxeTeHV"
  },
  "subscription_info": {
    "object": "list",
    "has_more": false,
    "url": "/v1/customers/1/subscriptions",
    "data": [
      {
        "id": "sub_6fiIsrRmV7tC9C",
        "plan": {
          "id": "JTA",
          "interval": "year",
          "name": "JellyTelly Annual Subscription",
          "created": 1435255142,
          "amount": 4000,
          "currency": "usd",
          "object": "plan",
          "livemode": false,
          "interval_count": 1,
          "trial_period_days": 7,
          "metadata": {},
          "statement_descriptor": "jellytellysubscription"
        },
        "object": "subscription",
        "start": 1437808478,
        "status": "active",
        "customer": "1",
        "cancel_at_period_end": false,
        "current_period_start": 1438413278,
        "current_period_end": 1470035678,
        "ended_at": null,
        "trial_start": 1437808478,
        "trial_end": 1438413278,
        "canceled_at": null,
        "quantity": 1,
        "application_fee_percent": null,
        "discount": {
          "coupon": {
            "id": "10OFF",
            "created": 1435255193,
            "percent_off": 10,
            "amount_off": null,
            "currency": null,
            "object": "coupon",
            "livemode": false,
            "duration": "forever",
            "redeem_by": null,
            "max_redemptions": null,
            "times_redeemed": 5,
            "duration_in_months": null,
            "valid": true,
            "metadata": {}
          },
          "start": 1437809621,
          "object": "discount",
          "customer": "1",
          "subscription": "sub_6fiIsrRmV7tC9C",
          "end": null
        },
        "tax_percent": null,
        "metadata": {}
      }
    ]
  }
}
```

This endpoint retrieves a specific user, by either id or email.

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`GET /users/<ID> HTTP/1.1
Host: apidev.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
ID | String | The ID of the user to retrieve, which can be either integer id or string email | true

## Edit

```ruby

```

```shell
curl -X PUT -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/users/12?user[email]=tester@email.com&user[password]=newpassword&user[first_name]=Tester&user[last_name]=McTesterson&user[username]'
```

>The above command returns JSON structured like this:

```json
{
  "user": {
    "id": 12,
    "email": "tester@email.com",
    "auth_token": "auth_token"
  }
}
```

This endpoint allows the user to update their info that is tied to the user account

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`PUT /users/12?user[email]=tester@email.com&user[password]=newpassword&user[first_name]=Tester&user[last_name]=McTesterson HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
ID | String | The ID of the user to edit | true
user | Hash | The user hash object, all subsequent parameters must be passed in the user hash
user[email] | String | Email of the user | false
user[password] | String | User password, minimum length: 6 chars | false
user[first_name] | String | User first name | false
user[last_name] | String | User last name | false
user[username] | String | Username for login | false

## Delete

```ruby
User.delete
```

```shell
curl -X DELETE -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://apidev.jellytelly.com/users/12'
```

This method archives the user by changing the status to Canceled, resets the auth_token to an unknown value, and returns a 204. This is a User action.

<aside class="notice">NOTE: this method requires the auth_token</aside>
<aside class="warning">NOTE: this method does not actually delete the user</aside>

### HTTP Request

`DELETE /users/<ID> HTTP/1.1
Host: apidev.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
ID | String | The ID of the user to delete | true


## List favorites
```ruby

```

```shell
curl -X GET -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/users/1/favorites'
```

>The above command returns JSON structured like this:

```json
{  
   "favorites":[  
      {  
         "id":184,
         "created_at":"2015-07-14T16:59:17.498-05:00",
         "updated_at":"2015-07-14T16:59:17.503-05:00",
         "embed_code":"E5YzkycjrLejf9I2zIPn0bpeYO3iXSCP",
         "name":"Madame Blueberry",
         "description":"Let your kids spend a little time with Madame Blueberry and the rest of the Veggies and they\u0026#039;ll learn that \u0026quot;being greedy makes you grumpy -- but a thankful heart is a happy heart!\u0026quot;",
         "image_url":"http://cf.c.ooyala.com/E5YzkycjrLejf9I2zIPn0bpeYO3iXSCP/c2iSbFw6b5_lmbUn4xMDoxOmdtO40mAx",
         "duration":2224641,
         "asset_type":"video",
         "asset_status":"live",
         "asset_created_at":"2014-12-02T15:19:56.000-06:00",
         "asset_updated_at":"2015-04-16T12:44:48.000-05:00",
         "original_file_name":"Madame Blueberry for JT.mp4",
         "series_id":84,
         "featured":false
      }
   ]
}
```

Returns list of videos added to favorites by user

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`GET /users/1/favorites HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
user_id | String | Id of user | true

## Add Video to favorites

```ruby

```

```shell
curl -X POST -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/users/4/favorites?video_id=66'
```

Adds video to favorites; no return object, just 200 status

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`POST /users/4/favorites?video_id=66 HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
user_id | String | ID of user | true
id | String | ID for video | true

## Remove Video from favorites

```ruby

```

```shell
curl -X DELETE -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/users/4/favorites/66'
```

Removes video from favorites; no return object, just 200 status

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`DELETE /users/4/favorites/66 HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
user_id | String | ID of user | true
id | String | ID for video | true


## Add Series to favorites

```ruby

```

```shell
curl -X POST -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/users/4/add_favorites_series?series_id=82'
```

Adds all videos for series favorites; no return object, just 200 status

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`POST /users/4/add_favorites_series?series_id=82 HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
user_id | String | ID of user | true
series_id | String | ID for series | true

## Remove Series from favorites

```ruby

```

```shell
curl -X DELETE -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/users/4/remove_favorites_series?series_id=82'
```

Removes all videos for series from favorites; no return object, just 200 status

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`DELETE /users/4/remove_favorites_series?series_id=82 HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
user_id | String | ID of user | true
series_id | String | ID for series | true


## List Playlist
```ruby

```

```shell
curl -X GET -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/users/1/playlists'
```

>The above command returns JSON structured like this:

```json
{  
   "playlist":[  
      {  
         "id":184,
         "created_at":"2015-07-14T16:59:17.498-05:00",
         "updated_at":"2015-07-14T16:59:17.503-05:00",
         "embed_code":"E5YzkycjrLejf9I2zIPn0bpeYO3iXSCP",
         "name":"Madame Blueberry",
         "description":"Let your kids spend a little time with Madame Blueberry and the rest of the Veggies and they\u0026#039;ll learn that \u0026quot;being greedy makes you grumpy -- but a thankful heart is a happy heart!\u0026quot;",
         "image_url":"http://cf.c.ooyala.com/E5YzkycjrLejf9I2zIPn0bpeYO3iXSCP/c2iSbFw6b5_lmbUn4xMDoxOmdtO40mAx",
         "duration":2224641,
         "asset_type":"video",
         "asset_status":"live",
         "asset_created_at":"2014-12-02T15:19:56.000-06:00",
         "asset_updated_at":"2015-04-16T12:44:48.000-05:00",
         "original_file_name":"Madame Blueberry for JT.mp4",
         "series_id":84,
         "featured":false
      }
   ]
}
```

Returns list of videos added to playlist by user

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`GET /users/1/playlists HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
user_id | String | Id of user | true

## Add Video to Playlist

```ruby

```

```shell
curl -X POST -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/users/4/playlists?video_id=66'
```

Adds video to playlist; no return object, just 200 status

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`POST /users/4/playlists?video_id=66 HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
user_id | String | ID of user | true
id | String | ID for video | true

## Remove Video from Playlist

```ruby

```

```shell
curl -X DELETE -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/users/4/playlists/66'
```

Removes video from playlist; no return object, just 200 status

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`DELETE /users/4/playlists/66 HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
user_id | String | ID of user | true
id | String | ID for video | true


## Add Series to Playlist

```ruby

```

```shell
curl -X POST -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/users/4/add_playlist_series?series_id=82'
```

Adds all videos for series playlist; no return object, just 200 status

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`POST /users/4/add_playlist_series?series_id=82 HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
user_id | String | ID of user | true
series_id | String | ID for series | true

## Remove Series from Playlist

```ruby

```

```shell
curl -X DELETE -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/users/4/remove_playlist_series?series_id=82'
```

Removes all videos for series from playlist; no return object, just 200 status

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`DELETE /users/4/remove_playlist_series?series_id=82 HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
user_id | String | ID of user | true
series_id | String | ID for series | true


## Add / Update Video Rating

```ruby

```

```shell
curl -X POST -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/users/4/ratings?video_id=66&rating=3.5'
```

Adds rating to video; no return object, just 200 status

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`POST /users/4/ratings?video_id=66&rating=3.5 HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
user_id | String | ID of user | true
video_id | String | ID for video | true
rating | String | Value for rating | true


## Set Active Episode

```ruby

```

```shell
curl -X POST -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/users/1/set_active_episode?embed_code=dxeG41dTrpdi41J069c1syLsLsUQyk2U'
```

Sets active episode on user record; no return object, just 200 status

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`POST /users/1/set_active_episode?embed_code=dxeG41dTrpdi41J069c1syLsLsUQyk2U HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
user_id | String | ID of user | true
embed_code | String | Embed code of video | true
