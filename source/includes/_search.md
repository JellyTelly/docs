# Search

## Get Search results

```ruby

```

```shell
curl -X GET -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://apidev.jellytelly.dev/search?query=truth'
```

>The above command returns JSON structured like this:

```json
{
  "search_results": [
    {
      "object_type": "Series",
      "data": {
        "id": 2,
        "created_at": "2015-07-25T02:40:20.665-05:00",
        "updated_at": "2015-07-25T02:40:21.232-05:00",
        "embed_code": "84NXc3dDpTxWHWYZMgKzX_Og98PR80JV",
        "name": "The Last Chance Detectives",
        "displayName": "Last Chance Detectives",
        "description": "Mike, Ben, Winnie and Spence - also known as the Last Chance Detectives - solve mysteries in their small desert hometown of Ambrosia, Arizona in the search for truth. Along the way, they discover the importance of integrity, forgiveness, faith and more.",
        "imageUrl": "http://cf.c.ooyala.com/84NXc3dDpTxWHWYZMgKzX_Og98PR80JV/promo261777455",
        "popularity": 0,
        "episodeCount": null,
        "asset_type": "video",
        "duration": 5005,
        "external_id": null,
        "asset_created_at": "2015-03-27T11:10:48.000-05:00",
        "asset_updated_at": "2015-07-21T14:58:09.000-05:00",
        "asset_status": "live",
        "asset_hosted_at": null,
        "original_file_name": "Black Screen for matt.mov"
      }
    },
    {
      "object_type": "Series",
      "data": {
        "id": 66,
        "created_at": "2015-07-25T02:40:33.450-05:00",
        "updated_at": "2015-07-25T02:40:33.603-05:00",
        "embed_code": "x2c2VlczplrEFQyY2mv0Q_iDUpFr7r6v",
        "name": "Hillsong Kids",
        "displayName": "Hillsong Kids",
        "description": "Join the Hillsong Kids team as they learn what it means to be devoted to God through music, comedy and Biblical truth with music and segments from live praise and worship albums.",
        "imageUrl": "http://cf.c.ooyala.com/x2c2VlczplrEFQyY2mv0Q_iDUpFr7r6v/promo250376315",
        "popularity": 0,
        "episodeCount": null,
        "asset_type": "video",
        "duration": 6573,
        "external_id": null,
        "asset_created_at": "2015-02-16T11:33:15.000-06:00",
        "asset_updated_at": "2015-03-11T15:58:36.000-05:00",
        "asset_status": "live",
        "asset_hosted_at": null,
        "original_file_name": "BLACK TEST 22.mp4"
      }
    }
  ]
}
```

This endpoint takes the criteria provided and searches title and description for videos and series

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`GET /search?query=<CRITERIA> HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Description
--------- | -----------
query | The criteria that is being searched
