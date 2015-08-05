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

Parameter | Description
--------- | -----------
user_id | ID of user creating subscription

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

Parameter | Description
--------- | -----------
user_id | ID of user creating subscription
id | ID for the selected subscription


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

Parameter | Description
--------- | -----------
user_id | ID of user creating subscription
plan_id | ID of selected subscription level
first_name | Optional: User first name
last_name | Optional: User last name
payment_token | Optional: Token from merchant service containing payment information, this is not required for iOS users
coupon_code | Optional: ID of coupon
subscription_source | Optional: Source of user, available choices are: iOS, Android, Web
subscriber_account_id | Optional: Id to look up subscription details, this will be an ID provided by merchant

## Edit

```ruby

```

```shell
curl -X PATCH -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/users/1/subscriptions/sub_6e0X9Kq1yWCBXw?payment_token=tok_16SMewJDs1f4mwxy1vziPDOY&coupon_code=10OFF'
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

`PATCH /users/1/subscriptions/sub_6e0X9Kq1yWCBXw?payment_token=tok_16SMewJDs1f4mwxy1vziPDOY&coupon_code=10OFF HTTP/1.1
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

<aside class="notice">This is a blue note</aside>
<aside class="warning">This is a red note</aside>
<aside class="success">This is a green note</aside>

### HTTP Request

`DELETE /users/3/subscriptions/sub_6ZRmNCL9OvhLTX HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Description
--------- | -----------
user_id | ID of user creating subscription
id | ID of subscription