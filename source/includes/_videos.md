# Videos

## Get a single video

```ruby

```

```shell
curl -X GET -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/videos/1'

or

curl -X GET -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/videos/Sing Through the Bible'
```

>The above command returns JSON structured like this:

```json
{
  "video": {
    "id": 1,
    "created_at": "2015-07-25T02:40:39.909-05:00",
    "updated_at": "2015-08-03T18:21:26.479-05:00",
    "embed_code": "JiczY1djqKDafzRTLd4Raze4gaClSvND",
    "name": "Sing Through the Bible",
    "description": "Sing through the Bible with Buck Denver and Friends! 30 music videos take you from Genesis to Revelation in a musical journey featuring your favorite characters from What’s in the Bible? - The Fabulous Bentley Brothers, Clive and Ian, Sunday School Lady and more! Includes on-screen sing-along lyrics for all 30 music videos.",
    "image_url": "http://cf.c.ooyala.com/JiczY1djqKDafzRTLd4Raze4gaClSvND/vplNG22HDCZOrhEX4xMDoxOjB1O8AjAz",
    "duration": 3424257,
    "asset_type": "video",
    "asset_status": "live",
    "asset_created_at": "2015-07-10T13:59:11.000-05:00",
    "asset_updated_at": "2015-07-15T16:07:09.000-05:00",
    "original_file_name": "STTB_For JT.mp4",
    "series_id": 3,
    "featured": false,
    "episode": 1
  }
}
```

This endpoint returns video_info based video name or id. The id sent is checked for numericality to determine how to search for video

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`GET /videos/1 HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"

or

GET /videos/Sing Through the Bible HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
id | String | ID of video, can be either a number or string | true


## Get featured video

```ruby

```

```shell
curl -X GET -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/videos/featured/'
```

>The above command returns JSON structured like this:

```json
{  
   "video":{  
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
      "featured":true
   }
}
```

This endpoint returns video_info based on user having an active episode or video being flagged as featured. If the user has an active episode that video is returned instead of the video flagged as featured in the system.

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`GET /videos/featured/ HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`


## Get player embed token

```ruby

```

```shell
curl -X GET -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/videos/playerEmbedToken?video_embed_code=M2N3RwcDqo98egZnFGbTk-FvkJ32VDTc&player_id=OWVmODJmMjQ4NmU3NWI5NDNhNmNhNjFi&user_id=3'
```

>The above command returns JSON structured like this:

```json
{  
   "embed_token":"http://player.ooyala.com/sas/embed_token/OWVmODJmMjQ4NmU3NWI5NDNhNmNhNjFi/M2N3RwcDqo98egZnFGbTk-FvkJ32VDTc?account_id=3\u0026api_key=hpZzM615i0ji4siN0eiX3cOy2BeU.qpcP-\u0026expires=1437275726\u0026signature=dT7dlTmcS2PFxhQuUxw7nC8ZLb%2BzCTxt0j6wWjJvIy"
}
```

This endpoint returns a url to be used as a token in Ooyala player for XDR (Cross Device Resume). See the [Ooyala documentation](http://support.ooyala.com/developers/documentation/concepts/player_v3dev_authoverview.html) for instructions for creating the player that includes the token

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`GET /videos/playerEmbedToken?video_embed_code=<video_embed_code>&player_id=<player_id>&user_id=<user_id> HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
video_embed_code | String | Embed code for video | true
player_id | String | Id of player | true
user_id | String | Id of user | true


## Get video playback position

```ruby

```

```shell
curl -X GET -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/videos/playbackPosition?video_embed_code=M2N3RwcDqo98egZnFGbTk-FvkJ32VDTc&user_id=3'
```

>The above command returns JSON structured like this:

```json
{"playback_position":15587}
```

This endpoint returns playback position (in seconds) of video to be used in Ooyala player for XDR (Cross Device Resume).

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`GET /videos/playbackPosition?video_embed_code=<video_embed_code>&user_id=<user_id> HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
video_embed_code | String | Embed code for video | true
user_id | String | Id of user | true
