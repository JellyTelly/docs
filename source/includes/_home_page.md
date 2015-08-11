# Home

## Logged In

```ruby

```

```shell
curl -X GET -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'https://api.jellytelly.com/logged_in_home'
```

>The above command returns JSON structured like this:

```json
{
  "featured_video": [
    {
      "id": 541,
      "created_at": "2015-07-25T03:02:19.134-05:00",
      "updated_at": "2015-08-03T19:28:41.342-05:00",
      "embed_code": "toZDY4aTpNsEcNOj1CcehWZHjiibK3vO",
      "name": "Long Journey",
      "description": "Macky and his family risk the wrath of the Romans by taking two refugee girls into their home. Through their exploits and retelling of their people’s stories – Daniel and the Lions’ Den as well as Jesus and the Miraculous Catch of Fish – we learn the importance of being courageous and helping others.",
      "image_url": "http://cf.c.ooyala.com/toZDY4aTpNsEcNOj1CcehWZHjiibK3vO/9nZFQMepuQiumqNn4zMDoxOjBrO1v9_L",
      "duration": 1519652,
      "asset_type": "video",
      "asset_status": "live",
      "asset_created_at": "2013-12-06T14:10:38.000-06:00",
      "asset_updated_at": "2015-06-30T14:57:29.000-05:00",
      "original_file_name": "Friends and Heroes 1-H.264 for Jelly Telly 3000kbs copy.mov",
      "series_id": 80,
      "featured": true,
      "episode": 1
    }
  ],
  "popular_series": [
    {
      "id": 3,
      "created_at": "2015-07-25T02:59:50.620-05:00",
      "updated_at": "2015-08-11T00:54:36.488-05:00",
      "embed_code": "IwNXc3dDoGzBO_7d5sllw9EDepmOTAIz",
      "name": "Sing Through the BIble",
      "displayName": "Sing Through the Bible",
      "description": "Sing through the Bible with Buck Denver and Friends! 30 music videos take you from Genesis to Revelation in a musical journey featuring your favorite characters from What’s in the Bible? - The Fabulous Bentley Brothers, Clive and Ian, Sunday School Lady and more! Includes on-screen sing-along lyrics for all 30 music videos.",
      "imageUrl": "http://cf.c.ooyala.com/IwNXc3dDoGzBO_7d5sllw9EDepmOTAIz/promo261149814",
      "popularity": 34,
      "episodeCount": 1,
      "asset_type": "video",
      "duration": 5005,
      "external_id": null,
      "asset_created_at": "2015-03-27T11:10:39.000-05:00",
      "asset_updated_at": "2015-07-14T08:38:02.000-05:00",
      "asset_status": "live",
      "asset_hosted_at": null,
      "original_file_name": "Black Screen for matt.mov"
    }
  ],
  "new_episodes": [
    {
      "id": 3,
      "created_at": "2015-07-25T02:59:50.620-05:00",
      "updated_at": "2015-08-11T00:54:36.488-05:00",
      "embed_code": "IwNXc3dDoGzBO_7d5sllw9EDepmOTAIz",
      "name": "Sing Through the BIble",
      "displayName": "Sing Through the Bible",
      "description": "Sing through the Bible with Buck Denver and Friends! 30 music videos take you from Genesis to Revelation in a musical journey featuring your favorite characters from What’s in the Bible? - The Fabulous Bentley Brothers, Clive and Ian, Sunday School Lady and more! Includes on-screen sing-along lyrics for all 30 music videos.",
      "imageUrl": "http://cf.c.ooyala.com/IwNXc3dDoGzBO_7d5sllw9EDepmOTAIz/promo261149814",
      "popularity": 34,
      "episodeCount": 1,
      "asset_type": "video",
      "duration": 5005,
      "external_id": null,
      "asset_created_at": "2015-03-27T11:10:39.000-05:00",
      "asset_updated_at": "2015-07-14T08:38:02.000-05:00",
      "asset_status": "live",
      "asset_hosted_at": null,
      "original_file_name": "Black Screen for matt.mov"
    }
  ],
  "series_by_label": {
    "Adventures": [
      {
        "id": 85,
        "created_at": "2015-07-25T03:00:06.942-05:00",
        "updated_at": "2015-08-08T01:53:59.378-05:00",
        "embed_code": "k5cWVlczrBvbWz9KJEvyjqf3WDkTtBDO",
        "name": "321 Penguins!",
        "displayName": "321 Penguins",
        "description": "Twin siblings Jason and Michelle discover penguin figurines that come to life. They travel the world and outer space learning important biblical and moral lessons with their four funky penguin friends.",
        "imageUrl": "http://cf.c.ooyala.com/k5cWVlczrBvbWz9KJEvyjqf3WDkTtBDO/promo249759193",
        "popularity": 9,
        "episodeCount": 20,
        "asset_type": "video",
        "duration": 6573,
        "external_id": null,
        "asset_created_at": "2015-02-16T11:32:00.000-06:00",
        "asset_updated_at": "2015-03-06T14:47:00.000-06:00",
        "asset_status": "live",
        "asset_hosted_at": "",
        "original_file_name": "BLACK TEST 2.mp4"
      }
    ],
    "Ages 2-5": [...
    ],
    "Ages 5-8": [...
    ],
    "Ages 8 and Up": [...
    ],
    "All Ages": [...
    ],
    "Bible Stories": [...
    ],
    "Cartoons": [...
    ],
    "Christmas": [...
    ],
    "Educational": [...
    ],
    "History and Nature": [...
    ],
    "Holidays": [...
    ],
    "Live Action": [...
    ],
    "Movies": [...
    ],
    "Music and Art": [...
    ],
    "Parables": [...
    ],
    "Puppets": [...
    ],
    "Values": [...
    ]
  }
}
```

This endpoint returns all objects for the logged in home page: Featured Video, Popular Series, Series with new episodes, and Series by labels.

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`GET /logged_in_home HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`
