# Subscriptions

## List All

```ruby

```

```shell
curl -X GET -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/users/2/subscriptions'
```

>The above command returns JSON structured like this:

```json
{  
   "subscriptions":[  
      {  
         "id":"sub_6ZQfFkmuKIBaOZ",
         "plan":{  
            "id":"JTA",
            "interval":"year",
            "name":"JellyTelly Annual Subscription",
            "created":1435255142,
            "amount":4000,
            "currency":"usd",
            "object":"plan",
            "livemode":false,
            "interval_count":1,
            "trial_period_days":7,
            "metadata":{  

            },
            "statement_descriptor":"jellytellysubscription"
         },
         "object":"subscription",
         "start":1436359045,
         "status":"active",
         "customer":"2",
         "cancel_at_period_end":false,
         "current_period_start":1436963845,
         "current_period_end":1468586245,
         "ended_at":null,
         "trial_start":1436359045,
         "trial_end":1436963845,
         "canceled_at":null,
         "quantity":1,
         "application_fee_percent":null,
         "discount":null,
         "tax_percent":null,
         "metadata":{  

         }
      }
   ]
}
```

This endpoint returns all subscriptions for the user

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`GET /users/2/subscriptions HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
user_id | String | ID of user creating subscription | true

## Get Subscription

```ruby

```

```shell
curl -X GET -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/users/2/subscriptions/sub_6ZQfFkmuKIBaOZ'
```

>The above command returns JSON structured like this:

```json
{  
   "id":"sub_6ZQfFkmuKIBaOZ",
   "plan":{  
      "id":"JTA",
      "interval":"year",
      "name":"JellyTelly Annual Subscription",
      "created":1435255142,
      "amount":4000,
      "currency":"usd",
      "object":"plan",
      "livemode":false,
      "interval_count":1,
      "trial_period_days":7,
      "metadata":{  

      },
      "statement_descriptor":"jellytellysubscription"
   },
   "object":"subscription",
   "start":1436359045,
   "status":"active",
   "customer":"2",
   "cancel_at_period_end":false,
   "current_period_start":1436963845,
   "current_period_end":1468586245,
   "ended_at":null,
   "trial_start":1436359045,
   "trial_end":1436963845,
   "canceled_at":null,
   "quantity":1,
   "application_fee_percent":null,
   "discount":null,
   "tax_percent":null,
   "metadata":{  

   }
}
```

This endpoint returns the specified subscription for the user

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`GET /users/2/subscriptions/sub_6ZQfFkmuKIBaOZ HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
user_id | String ID of user creating subscription | true
id | String | ID for the selected subscription | true


## Create

```ruby

```

```shell
curl -X POST -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/users/12/subscriptions?first_name=Tester&last_name=McTesterson&plan_id=JTA&payment_token=tok_16SMewJDs1f4mwxy1vziPDOY&coupon_code=10OFF&subscription_source=Web&subscriber_account_id=abc123'
```

>The above command returns JSON structured like this:

```json
{  
   "id":"sub_6ZQfFkmuKIBaOZ",
   "plan":{  
      "id":"JTA",
      "interval":"year",
      "name":"JellyTelly Annual Subscription",
      "created":1435255142,
      "amount":4000,
      "currency":"usd",
      "object":"plan",
      "livemode":false,
      "interval_count":1,
      "trial_period_days":7,
      "metadata":{  

      },
      "statement_descriptor":"jellytellysubscription"
   },
   "object":"subscription",
   "start":1436359045,
   "status":"active",
   "customer":"2",
   "cancel_at_period_end":false,
   "current_period_start":1436963845,
   "current_period_end":1468586245,
   "ended_at":null,
   "trial_start":1436359045,
   "trial_end":1436963845,
   "canceled_at":null,
   "quantity":1,
   "application_fee_percent":null,
   "discount":null,
   "tax_percent":null,
   "metadata":{  

   }
}
```

This endpoint creates a subscription for the user, as well as updates their name

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`POST /users/12/subscriptions?first_name=Tester&last_name=McTesterson&plan_id=JTA&payment_token=tok_16SMewJDs1f4mwxy1vziPDOY&coupon_code=10OFF&subscription_source=Web&subscriber_account_id=abc123 HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
user_id | String | ID of user creating subscription | true
plan_id | String | ID of selected subscription level | true
first_name | String | User first name | true
last_name | String | User last name | true
payment_token | String | Token from merchant service containing payment information, this is not required for iOS users | false
coupon_code | String | ID of coupon | false
subscription_source | String | Source of user, available choices are: iOS, Android, Web. Web is default | false
subscriber_account_id | String | Id to look up subscription details, this will be an ID provided by merchant | false

## Edit

```ruby

```

```shell
curl -X PUT -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/users/1/subscriptions/sub_6e0X9Kq1yWCBXw?payment_token=tok_16SMewJDs1f4mwxy1vziPDOY&coupon_code=10OFF'
```

>The above command returns JSON structured like this:

```json
{  
   "id":"sub_6ZQfFkmuKIBaOZ",
   "plan":{  
      "id":"JTA",
      "interval":"year",
      "name":"JellyTelly Annual Subscription",
      "created":1435255142,
      "amount":4000,
      "currency":"usd",
      "object":"plan",
      "livemode":false,
      "interval_count":1,
      "trial_period_days":7,
      "metadata":{  

      },
      "statement_descriptor":"jellytellysubscription"
   },
   "object":"subscription",
   "start":1436359045,
   "status":"active",
   "customer":"2",
   "cancel_at_period_end":false,
   "current_period_start":1436963845,
   "current_period_end":1468586245,
   "ended_at":null,
   "trial_start":1436359045,
   "trial_end":1436963845,
   "canceled_at":null,
   "quantity":1,
   "application_fee_percent":null,
   "discount":null,
   "tax_percent":null,
   "metadata":{  

   }
}
```

This endpoint updates the subscription to either monthly or annual, and applies a coupon

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`PUT /users/1/subscriptions/sub_6e0X9Kq1yWCBXw?payment_token=tok_16SMewJDs1f4mwxy1vziPDOY&coupon_code=10OFF HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Description
--------- | -----------
user_id | ID of user creating subscription
id | ID of subscription
payment_token | Optional: Token from merchant service containing payment information, this is not required for iOS users
coupon_code | Optional: ID of coupon


## Delete

```ruby

```

```shell
curl -X DELETE -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/users/3/subscriptions/sub_6ZRmNCL9OvhLTX'
```

This end removes the user subscription, and sets the user role to "user", then returns a 204

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`DELETE /users/3/subscriptions/sub_6ZRmNCL9OvhLTX HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Description
--------- | -----------
user_id | ID of user creating subscription
id | ID of subscription


## List Available Plans

```ruby

```

```shell
curl -X GET -H "Cache-Control: no-cache" 'https://api.jellytelly.com/subscription/plans'
```

>The above command returns JSON structured like this:

```json
{
  "plans": [
    {
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
    {
      "id": "JTM",
      "interval": "month",
      "name": "JellyTelly Monthly Subscription",
      "created": 1435255086,
      "amount": 500,
      "currency": "usd",
      "object": "plan",
      "livemode": false,
      "interval_count": 1,
      "trial_period_days": 7,
      "metadata": {},
      "statement_descriptor": "Jellytellysubscription"
    }
  ]
}
```

This endpoint returns all available subscription plans


### HTTP Request

`GET /subscription/plans HTTP/1.1
Host: api.jellytelly.com
Cache-Control: no-cache`
