# Series

## Get an individual series

```ruby

```

```shell
curl -X GET -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/series/VeggieTales'
```

>The above command returns JSON structured like this:

```json
{
  "series_info": {
    "id": 87,
    "created_at": "2015-07-25T02:40:37.302-05:00",
    "updated_at": "2015-07-25T02:40:37.543-05:00",
    "embed_code": "k1cWVlczroGjw0tvMyA7Ij2_d5LZdy3D",
    "name": "VeggieTales",
    "displayName": "VeggieTales",
    "description": "Watch these select episodes as Bob the Tomato, Larry the Cucumber and all their veggie friends engage in fun stories and songs that teach Biblical values!",
    "imageUrl": "http://cf.c.ooyala.com/k1cWVlczroGjw0tvMyA7Ij2_d5LZdy3D/promo249759216",
    "popularity": 0,
    "episodeCount": null,
    "asset_type": "video",
    "duration": 6573,
    "external_id": null,
    "asset_created_at": "2015-02-16T11:32:00.000-06:00",
    "asset_updated_at": "2015-03-06T14:46:57.000-06:00",
    "asset_status": "live",
    "asset_hosted_at": null,
    "original_file_name": "BLACK TEST 1.mp4"
  },
  "videos": [
    {
      "series_id": 87,
      "id": 185,
      "created_at": "2015-07-25T02:41:14.818-05:00",
      "updated_at": "2015-08-03T18:22:14.418-05:00",
      "embed_code": "E5YzkycjrLejf9I2zIPn0bpeYO3iXSCP",
      "name": "Madame Blueberry",
      "description": "Let your kids spend a little time with Madame Blueberry and the rest of the Veggies and they&#039;ll learn that &quot;being greedy makes you grumpy -- but a thankful heart is a happy heart!&quot;",
      "image_url": "http://cf.c.ooyala.com/E5YzkycjrLejf9I2zIPn0bpeYO3iXSCP/c2iSbFw6b5_lmbUn4xMDoxOmdtO40mAx",
      "duration": 2224641,
      "asset_type": "video",
      "asset_status": "live",
      "asset_created_at": "2014-12-02T15:19:56.000-06:00",
      "asset_updated_at": "2015-04-16T12:44:48.000-05:00",
      "original_file_name": "Madame Blueberry for JT.mp4",
      "featured": false,
      "episode": 1
    },
    {
      "series_id": 87,
      "id": 187,
      "created_at": "2015-07-25T02:41:15.165-05:00",
      "updated_at": "2015-08-03T18:22:14.901-05:00",
      "embed_code": "w2bTgycjpeLNDcea39RQYE00PhlC56Ni",
      "name": "Moe and the Big Exit",
      "description": "Saddle up for western adventure as Moe (Larry the Cucumber) brings us a lesson in following directions.",
      "image_url": "http://cf.c.ooyala.com/w2bTgycjpeLNDcea39RQYE00PhlC56Ni/T6d-rUZNqcn4uJqH4xMDoxOjBzMTt2bJ",
      "duration": 3050383,
      "asset_type": "video",
      "asset_status": "live",
      "asset_created_at": "2014-12-02T15:02:59.000-06:00",
      "asset_updated_at": "2015-04-16T12:45:28.000-05:00",
      "original_file_name": "Veggietales - Moe Big Exit.mp4",
      "featured": false,
      "episode": 2
    },
    {
      "series_id": 87,
      "id": 188,
      "created_at": "2015-07-25T02:41:15.390-05:00",
      "updated_at": "2015-08-03T18:22:15.192-05:00",
      "embed_code": "YweTYycjqcYH3Xdsmgi8EOQIcxh20kMR",
      "name": "Dave and the Giant Pickle",
      "description": "While little shepherd boy Dave is made to feel small by his brothers, everyone finds out that their foe is much bigger than they thought! Is anyone big enough to take on a 9-foot pickle? Dave learns that \"with God, all things are possible!\"",
      "image_url": "http://cf.c.ooyala.com/YweTYycjqcYH3Xdsmgi8EOQIcxh20kMR/m3ijHmCxBlAEKp8H4xMDoxOmdtO40mAx",
      "duration": 1686770,
      "asset_type": "video",
      "asset_status": "live",
      "asset_created_at": "2014-12-02T14:14:26.000-06:00",
      "asset_updated_at": "2015-06-15T11:09:06.000-05:00",
      "original_file_name": "Veggietales - Dave Giant Pickle.mp4",
      "featured": false,
      "episode": 3
    },
    {
      "series_id": 87,
      "id": 189,
      "created_at": "2015-07-25T02:41:15.595-05:00",
      "updated_at": "2015-08-03T18:22:15.494-05:00",
      "embed_code": "Z5ZDUycjo8B5WwTtJY2sBPoKdybkf7_y",
      "name": "Esther: The Girl Who Became Queen",
      "description": "Esther has been chosen by the King to be Queen, but she’s about to find out that the job will take more courage than she ever imagined! Esther: The Girl Who Became Queen teaches kids that “you never need to be afraid to do what’s right!”",
      "image_url": "http://cf.c.ooyala.com/Z5ZDUycjo8B5WwTtJY2sBPoKdybkf7_y/FM2ZbPgo9ocuVTrX4xMDoxOmdtO40mAx",
      "duration": 2370303,
      "asset_type": "video",
      "asset_status": "live",
      "asset_created_at": "2014-12-02T13:09:50.000-06:00",
      "asset_updated_at": "2015-04-16T12:44:04.000-05:00",
      "original_file_name": "Veggietales - Esther.mp4",
      "featured": false,
      "episode": 4
    },
    {
      "series_id": 87,
      "id": 190,
      "created_at": "2015-07-25T02:41:15.804-05:00",
      "updated_at": "2015-08-03T18:22:15.725-05:00",
      "embed_code": "hjNGoxcjqloxO0CT_9ldyIOS7ROzdMiC",
      "name": "King George and the Ducky",
      "description": "Unlike other kings, King George spends most of his time ... in the bathtub! That's where he plays with his favorite toy: his rubber ducky. But one ducky isn't enough for King George-- he wants all the duckies in the kingdom! Can he learn to put others first before it's too late?",
      "image_url": "http://cf.c.ooyala.com/hjNGoxcjqloxO0CT_9ldyIOS7ROzdMiC/Y_A4N2V4-G_UMyZH4xMDoxOmdtO40mAx",
      "duration": 2150316,
      "asset_type": "video",
      "asset_status": "live",
      "asset_created_at": "2014-12-01T15:06:20.000-06:00",
      "asset_updated_at": "2015-05-12T13:47:18.000-05:00",
      "original_file_name": "Veggietales - King George.mp4",
      "featured": false,
      "episode": 5
    },
    {
      "series_id": 87,
      "id": 191,
      "created_at": "2015-07-25T02:41:15.999-05:00",
      "updated_at": "2015-08-03T18:22:15.946-05:00",
      "embed_code": "sxeWcxcjo4lrXN4sSiI-S2erHRTzpnzK",
      "name": "The Ballad of Little Joe",
      "description": "Now, y’all have heard the story of Joseph and his coat of many colors before, but I reckon you’ve never heard it told as a Western… until now.",
      "image_url": "http://cf.c.ooyala.com/sxeWcxcjo4lrXN4sSiI-S2erHRTzpnzK/qLYPP9OxJMjaV9jn4zMDoxOjBzMTu0hl",
      "duration": 2191399,
      "asset_type": "video",
      "asset_status": "live",
      "asset_created_at": "2014-12-01T13:28:40.000-06:00",
      "asset_updated_at": "2015-04-16T12:44:22.000-05:00",
      "original_file_name": "LITTLE JOE UPDATED.mp4",
      "featured": false,
      "episode": 6
    }
  ]
}
```

This endpoint returns series_info based on either series displayName or id. The id sent is checked for numericality to determine how to search for series

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`GET /series/<id> HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
id | String | Can be either a number or string | true

## Get Popular series

```ruby

```

```shell
curl -X GET -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/series/popular?limit=2'
```

>The above command returns JSON structured like this:

```json
{
  "series_info": [
    {
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
    },
    {
      "id": 1,
      "created_at": "2015-07-25T02:40:20.415-05:00",
      "updated_at": "2015-07-25T02:40:20.661-05:00",
      "embed_code": "JzNXc3dDoP8EIOf_UNyWPCqUdp31CGSR",
      "name": "Janet's Planet",
      "displayName": "Janets Planet",
      "description": "Traveling at the speed of thought, join Janet on her adventures as she learns about science and health.",
      "imageUrl": "http://cf.c.ooyala.com/JzNXc3dDoP8EIOf_UNyWPCqUdp31CGSR/promo261777615",
      "popularity": 0,
      "episodeCount": null,
      "asset_type": "video",
      "duration": 5005,
      "external_id": null,
      "asset_created_at": "2015-03-27T11:11:08.000-05:00",
      "asset_updated_at": "2015-07-21T15:10:22.000-05:00",
      "asset_status": "live",
      "asset_hosted_at": null,
      "original_file_name": "Black Screen for matt.mov"
    }
  ]
}
```

This endpoint returns series_info based on popularity limited to number sent in

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`GET /series/popular?limit=<limit> HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
limit | String | limit controls the number of series to return | true


## Get New Series

```ruby

```

```shell
curl -X GET -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/series/new_episodes'
```

>The above command returns JSON structured like this:

```json
{
  "series_info": [
    {
      "id": 3,
      "created_at": "2015-07-25T02:40:21.237-05:00",
      "updated_at": "2015-07-25T02:40:21.431-05:00",
      "embed_code": "IwNXc3dDoGzBO_7d5sllw9EDepmOTAIz",
      "name": "Sing Through the BIble",
      "displayName": "Sing Through the Bible",
      "description": "Sing through the Bible with Buck Denver and Friends! 30 music videos take you from Genesis to Revelation in a musical journey featuring your favorite characters from What’s in the Bible? - The Fabulous Bentley Brothers, Clive and Ian, Sunday School Lady and more! Includes on-screen sing-along lyrics for all 30 music videos.",
      "imageUrl": "http://cf.c.ooyala.com/IwNXc3dDoGzBO_7d5sllw9EDepmOTAIz/promo261149814",
      "popularity": 0,
      "episodeCount": null,
      "asset_type": "video",
      "duration": 5005,
      "external_id": null,
      "asset_created_at": "2015-03-27T11:10:39.000-05:00",
      "asset_updated_at": "2015-07-14T08:38:02.000-05:00",
      "asset_status": "live",
      "asset_hosted_at": null,
      "original_file_name": "Black Screen for matt.mov"
    },
    {
      "id": 10,
      "created_at": "2015-07-25T02:40:22.597-05:00",
      "updated_at": "2015-07-25T02:40:22.952-05:00",
      "embed_code": "5pZWwxdDrVu6LMH95YsJ4FfFgVUKdukT",
      "name": "The Power of Same",
      "displayName": "The Power of Same",
      "description": "Millions of miles above the earth, in a spacecraft that can navigate space storms, supernovas, and the sun, Astrohost Kyle teaches all about the power of self-discipline and building healthy habits.",
      "imageUrl": "http://cf.c.ooyala.com/5pZWwxdDrVu6LMH95YsJ4FfFgVUKdukT/promo252777728",
      "popularity": 0,
      "episodeCount": null,
      "asset_type": "video",
      "duration": 5071,
      "external_id": null,
      "asset_created_at": "2015-03-17T13:28:53.000-05:00",
      "asset_updated_at": "2015-07-14T08:42:17.000-05:00",
      "asset_status": "live",
      "asset_hosted_at": null,
      "original_file_name": "BLACK SCREEN FOR MATT.mp4"
    },
    {
      "id": 12,
      "created_at": "2015-07-25T02:40:23.130-05:00",
      "updated_at": "2015-07-25T02:40:23.332-05:00",
      "embed_code": "NwOWwxdDqakm6e-HkyMY5wKbtPTQ6EXM",
      "name": "The Finders: Warehouse 110",
      "displayName": "The Finders Warehouse 110",
      "description": "A mysterious delivery sends the Finders into the dark rooms of Warehouse 110, a property that is steeped in history and comes with legends of a treasure and it's very own pirate ghost. In Warehouse 110, The Finders must work together to find the deed, save the warehouse, and find the treasure before someone else - or something else - gets there first.",
      "imageUrl": "http://cf.c.ooyala.com/NwOWwxdDqakm6e-HkyMY5wKbtPTQ6EXM/promo252777758",
      "popularity": 0,
      "episodeCount": null,
      "asset_type": "video",
      "duration": 5071,
      "external_id": null,
      "asset_created_at": "2015-03-17T13:23:05.000-05:00",
      "asset_updated_at": "2015-07-14T08:44:34.000-05:00",
      "asset_status": "live",
      "asset_hosted_at": null,
      "original_file_name": "BLACK SCREEN FOR MATT.mp4"
    },
    {
      "id": 11,
      "created_at": "2015-07-25T02:40:22.956-05:00",
      "updated_at": "2015-07-25T02:40:23.125-05:00",
      "embed_code": "BhYWwxdDor7PR4M6Ip2kb9Rhtd1iDaWq",
      "name": "The Adventures of Sam E. Sprocket",
      "displayName": "The Adventures of Sam E Sprocket",
      "description": "Sam E. Sprocket is a brave space traveler, but if he can't learn from the Bible how to be a Power Protector, he'll never collect enough fuel stars to keep his spaceship moving! In The Adventures of Sam E. Sprocket, Sam E. and his computer, Meep, work together to learn from God's Word and make it home safely.",
      "imageUrl": "http://cf.c.ooyala.com/BhYWwxdDor7PR4M6Ip2kb9Rhtd1iDaWq/promo252777744",
      "popularity": 0,
      "episodeCount": null,
      "asset_type": "video",
      "duration": 5071,
      "external_id": null,
      "asset_created_at": "2015-03-17T13:23:33.000-05:00",
      "asset_updated_at": "2015-07-14T08:42:55.000-05:00",
      "asset_status": "live",
      "asset_hosted_at": null,
      "original_file_name": "BLACK SCREEN FOR MATT.mp4"
    },
    {
      "id": 6,
      "created_at": "2015-07-25T02:40:21.814-05:00",
      "updated_at": "2015-07-25T02:40:22.013-05:00",
      "embed_code": "F5M3c3dDoV5FGOkh7D1aqGnl-r5YEESe",
      "name": "Sticks and Stones",
      "displayName": "Sticks and Stones",
      "description": "In Sticks & Stones, Pastor Frank uses ancient weapons to teach about big faith from the story of David and Goliath.",
      "imageUrl": "http://cf.c.ooyala.com/F5M3c3dDoV5FGOkh7D1aqGnl-r5YEESe/promo252777621",
      "popularity": 0,
      "episodeCount": null,
      "asset_type": "video",
      "duration": 5005,
      "external_id": null,
      "asset_created_at": "2015-03-27T11:09:44.000-05:00",
      "asset_updated_at": "2015-07-14T08:41:15.000-05:00",
      "asset_status": "live",
      "asset_hosted_at": null,
      "original_file_name": "Black Screen for matt.mov"
    },
    {
      "id": 9,
      "created_at": "2015-07-25T02:40:22.382-05:00",
      "updated_at": "2015-07-25T02:40:22.593-05:00",
      "embed_code": "oyM3c3dDpwYWx7U8xk-jRWvBeLHhTnW9",
      "name": "Oldman and Spielman's Christmastime Adventure",
      "displayName": "Oldman and Spielmans Christmastime Adventure",
      "description": "In Oldman and Spielman's Christmas Adventure, Doctor Oldman and his former nemesis, Oscar Spielman, take their Christmas musical to Broadway. When something very important gets left behind, their big adventure leads them to a deeper understanding of God's love and a musical finale in Central Park.",
      "imageUrl": "http://cf.c.ooyala.com/oyM3c3dDpwYWx7U8xk-jRWvBeLHhTnW9/promo252777696",
      "popularity": 0,
      "episodeCount": null,
      "asset_type": "video",
      "duration": 5005,
      "external_id": null,
      "asset_created_at": "2015-03-27T11:08:31.000-05:00",
      "asset_updated_at": "2015-07-14T08:44:13.000-05:00",
      "asset_status": "live",
      "asset_hosted_at": null,
      "original_file_name": "Black Screen for matt.mov"
    },
    {
      "id": 7,
      "created_at": "2015-07-25T02:40:22.018-05:00",
      "updated_at": "2015-07-25T02:40:22.216-05:00",
      "embed_code": "Z1M3c3dDoqys1bY79ZFVReOffp3yN-HB",
      "name": "Calling Sticks and Stones",
      "displayName": "Calling Sticks and Stones",
      "description": "Eugene Sticks and his hilarious sidekick, Stones, read Bible stories and make collectible crafts using only sticks and stones on their very own talk show.",
      "imageUrl": "http://cf.c.ooyala.com/Z1M3c3dDoqys1bY79ZFVReOffp3yN-HB/promo252777651",
      "popularity": 0,
      "episodeCount": null,
      "asset_type": "video",
      "duration": 5005,
      "external_id": null,
      "asset_created_at": "2015-03-27T11:09:33.000-05:00",
      "asset_updated_at": "2015-07-14T08:41:28.000-05:00",
      "asset_status": "live",
      "asset_hosted_at": null,
      "original_file_name": "Black Screen for matt.mov"
    }
  ]
}
```

This endpoint returns series_info based on there being new shows added in the last 90 days

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`GET /series/new_episodes HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

## Get series by label

```ruby

```

```shell
curl -X GET -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/series/bylabel?label=Adventures,Puppets'
```

>The above command returns JSON structured like this:

```json
{
  "Adventures": [
    {
      "id": 37,
      "created_at": "2015-07-25T02:40:28.212-05:00",
      "updated_at": "2015-07-25T02:40:28.381-05:00",
      "embed_code": "42Nndmczp8jbf7cGjxsTTC43G0RsZ8j2",
      "name": "What Katy Did",
      "displayName": "What Katy Did",
      "description": "Katy, a headstrong, energetic thirteen-year-old girl with a feisty, rebellious streak who seems to be more than her father can handle at times. The arrival of her ill cousin begins to alter Katy's perception of the world.",
      "imageUrl": "http://cf.c.ooyala.com/42Nndmczp8jbf7cGjxsTTC43G0RsZ8j2/promo248546696",
      "popularity": 0,
      "episodeCount": null,
      "asset_type": "video",
      "duration": 11583,
      "external_id": null,
      "asset_created_at": "2015-02-17T13:11:45.000-06:00",
      "asset_updated_at": "2015-03-03T11:39:12.000-06:00",
      "asset_status": "live",
      "asset_hosted_at": null,
      "original_file_name": "BLACK SCREEN TEST 9.mp4"
    },
    {
      "id": 5,
      "created_at": "2015-07-25T02:40:21.621-05:00",
      "updated_at": "2015-07-25T02:40:21.810-05:00",
      "embed_code": "szNHc3dDqbJaI_OcljtKqO4PN1watrz5",
      "name": "Zack In Time",
      "displayName": "Zack In Time",
      "description": "Zack Martin doesn't do Christmas. His friend, Doctor Oldman, can't get enough red and green. Zack in Time follows this unlikely pair through time on a bright red, time-traveling motorcycle, where Zack doesn't just get a taste of the wild west and disco fever, but learns to love his family and their timeless Christmas traditions.",
      "imageUrl": "http://cf.c.ooyala.com/szNHc3dDqbJaI_OcljtKqO4PN1watrz5/promo252777603",
      "popularity": 0,
      "episodeCount": null,
      "asset_type": "video",
      "duration": 5005,
      "external_id": null,
      "asset_created_at": "2015-03-27T11:10:00.000-05:00",
      "asset_updated_at": "2015-07-14T08:40:51.000-05:00",
      "asset_status": "live",
      "asset_hosted_at": null,
      "original_file_name": "Black Screen for matt.mov"
    }
  ]
}
```

This endpoint returns series_info based on label

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`GET /series/bylabel?label=<label> HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
label | String | Available labels are from list of v3 labels, see listLabels method | true

## List available labels

```ruby

```

```shell
curl -X GET -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/labels'
```

>The above command returns JSON structured like this:

```json
{  
   "labels":[  
      {  
         "id":19,
         "value":"Adventures"
      },
      {  
         "id":18,
         "value":"Ages 2-5"
      },
      {  
         "id":17,
         "value":"Ages 5-8"
      },
      {  
         "id":16,
         "value":"Ages 8 and Up"
      },
      {  
         "id":15,
         "value":"All Ages"
      },
      {  
         "id":14,
         "value":"Bible Stories"
      },
      {  
         "id":13,
         "value":"Cartoons"
      },
      {  
         "id":12,
         "value":"Christmas"
      },
      {  
         "id":11,
         "value":"Educational"
      },
      {  
         "id":10,
         "value":"En Espanol"
      },
      {  
         "id":9,
         "value":"Featured"
      },
      {  
         "id":8,
         "value":"History and Nature"
      },
      {  
         "id":7,
         "value":"Holidays"
      },
      {  
         "id":6,
         "value":"Live Action"
      },
      {  
         "id":20,
         "value":"Logged Out Home"
      },
      {  
         "id":5,
         "value":"Movies"
      },
      {  
         "id":4,
         "value":"Music and Art"
      },
      {  
         "id":3,
         "value":"Parables"
      },
      {  
         "id":2,
         "value":"Puppets"
      },
      {  
         "id":1,
         "value":"Values"
      }
   ]
}
```

This endpoint returns list of label id and values to be used to find series by label

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`GET /labels HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`
