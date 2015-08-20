# Coupons

## View Coupon Detail

```ruby

```

```shell
curl -X GET -H "Cache-Control: no-cache" 'https://api.jellytelly.com/coupons/10OFF'
```

>The above command returns JSON structured like this:

```json
Success:
{
  "coupon_info": {
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
    "times_redeemed": 71,
    "duration_in_months": null,
    "valid": true,
    "metadata": {}
  }
}

Error:
{
  "errors": {
    "message": "No such coupon: 10OF",
    "http_status": 404,
    "http_body": "{\n  \"error\": {\n    \"type\": \"invalid_request_error\",\n    \"message\": \"No such coupon: 10OF\",\n    \"param\": \"id\"\n  }\n}\n",
    "http_headers": {
      "server": "nginx",
      "date": "Thu, 20 Aug 2015 15:08:20 GMT",
      "content_type": "application/json",
      "content_length": "115",
      "connection": "keep-alive",
      "access_control_allow_credentials": "true",
      "access_control_allow_methods": "GET, POST, HEAD, OPTIONS, DELETE",
      "access_control_allow_origin": "*",
      "access_control_max_age": "300",
      "cache_control": "no-cache, no-store",
      "request_id": "req_6pZoZaH6zibboh",
      "stripe_version": "2015-07-28"
    },
    "json_body": {
      "error": {
        "type": "invalid_request_error",
        "message": "No such coupon: 10OF",
        "param": "id"
      }
    },
    "request_id": "req_6pZoZaH6zibboh",
    "param": "id"
  }
}
```

This endpoint returns information about a coupon. If valid coupon data is returned, there are two values to be checked, percent_off or amount_off, but only one should have data.

### HTTP Request

`GET /coupons/10OFF HTTP/1.1
Host: api.jellytelly.com
Cache-Control: no-cache`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
id | String | Id for coupon | true
