# Users

## Get a Specific User

```ruby
class User < Jellytelly
  ...

  get :find, '/users/:id'

  ...
end

u = User.find(2)
```

```shell
curl "http://api.jellytelly.com/users/2"
  -H 'Authorization: Token token="auth_token"'
```

> The above command returns JSON structured like this:

```json
{
  "user_info": {
    "subscription_source": "Web",
    "subscriber_account_id": "1",
    "id": 1,
    "email": "john.henderson@creativetrust.com",
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
    "first_name": "John",
    "last_name": "Henderson",
    "username": "john.henderson@creativetrust.com"
  },
  "billing_info": {
    "id": "1",
    "object": "customer",
    "created": 1437808306,
    "livemode": false,
    "description": null,
    "email": "john.henderson@creativetrust.com",
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

This endpoint retrieves a specific user.

<aside class="warning">If you're not using an administrator API key, note that some users will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET http://example.com/users/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the user to retrieve
