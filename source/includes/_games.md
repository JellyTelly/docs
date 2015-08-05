# Games

## List all games

```ruby

```

```shell
curl -X GET -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/games'
```

>The above command returns JSON structured like this:

```json
{
  "games_info": [
    {
      "id": 1,
      "title": "Zap!",
      "description": "Challenge your friends and family in 2 player mode to see who has the fastest reaction time or see if you have what it takes to beat Zap on insane hard!",
      "category": "Challenges",
      "age": "All",
      "game_type": "HTML5",
      "file_name": "zap",
      "created_at": "2015-07-19T19:00:00.000-05:00",
      "updated_at": "2015-07-19T19:00:00.000-05:00"
    },
    {
      "id": 2,
      "title": "Agnes & Winnie's Big Air",
      "description": "Take to the slopes with Agnes and Winnie and earn big points for the coolest snow boarding tricks.",
      "category": "Challenges",
      "age": "5-8, 8+",
      "game_type": "Flash",
      "file_name": "big_air",
      "created_at": "2015-07-19T19:00:00.000-05:00",
      "updated_at": "2015-07-19T19:00:00.000-05:00"
    },
    {
      "id": 3,
      "title": "Air Adventures with Clive and Ian",
      "description": "Watch out for lions and monkeys as you fly the wild skies with Clive and Ian.",
      "category": "Challenges",
      "age": "5-8, 8+",
      "game_type": "Flash",
      "file_name": "air_adventures",
      "created_at": "2015-07-19T19:00:00.000-05:00",
      "updated_at": "2015-07-19T19:00:00.000-05:00"
    },
    {
      "id": 4,
      "title": "Dr. SchniffenHousen’s Alarm in the Lab",
      "description": "Watch out for flying cats while you help Dr. Schniffenhousen catch his falling beakers.",
      "category": "Challenges",
      "age": "5-8, 8+",
      "game_type": "Flash",
      "file_name": "alarm",
      "created_at": "2015-07-19T19:00:00.000-05:00",
      "updated_at": "2015-07-19T19:00:00.000-05:00"
    },
    {
      "id": 5,
      "title": "Pirate Parachute with Captain Pete",
      "description": "Collect treasure with Captain Pete but don’t let the treasure or the clouds get caught in his parachute.",
      "category": "Challenges",
      "age": "5-8, 8+",
      "game_type": "Flash",
      "file_name": "pirate-parachute",
      "created_at": "2015-07-19T19:00:00.000-05:00",
      "updated_at": "2015-07-19T19:00:00.000-05:00"
    },
    {
      "id": 6,
      "title": "Captain Pete’s Treasure Hunt",
      "description": "It's time to go hunting for treasure with Captain Pete from What's In the Bible?! Go fishing with Captain Pete and collect 'Pearls of Wisdom' along the way, which helps the player learn Bible verses!",
      "category": "Learn Scripture",
      "age": "5-8, 8+",
      "game_type": "HTML5",
      "file_name": "captain-petes-treasure-hunt",
      "created_at": "2015-07-19T19:00:00.000-05:00",
      "updated_at": "2015-07-19T19:00:00.000-05:00"
    },
    {
      "id": 7,
      "title": "Armor of God",
      "description": "Join the adventure to collect all the pieces of the Armor of God!",
      "category": "Learn Scripture",
      "age": "5-8, 8+",
      "game_type": "HTML5",
      "file_name": "armor-up",
      "created_at": "2015-07-19T19:00:00.000-05:00",
      "updated_at": "2015-07-19T19:00:00.000-05:00"
    },
    {
      "id": 8,
      "title": "Memory Mountain",
      "description": "Do you have what it takes to climb Memory Mountain? Memorize ten verses that span the Old and New Testament and see if you have what it takes to make to make it to the top! Challenge your friends and family to see who can climb Memory Mountain the fastest!",
      "category": "Learn Scripture",
      "age": "5-8, 8+",
      "game_type": "HTML5",
      "file_name": "memory-mountain",
      "created_at": "2015-07-19T19:00:00.000-05:00",
      "updated_at": "2015-07-19T19:00:00.000-05:00"
    },
    {
      "id": 9,
      "title": "Bible What’s It? With Chester Whigget",
      "description": "Chester Whigget from What's In the Bible? wants to challenge you to Bible trivia! Test your knowledge of the Bible with these questions from Chester and see if you can get a perfect score!",
      "category": "Learn Scripture",
      "age": "5-8, 8+",
      "game_type": "HTML5",
      "file_name": "bible-whats-it",
      "created_at": "2015-07-19T19:00:00.000-05:00",
      "updated_at": "2015-07-19T19:00:00.000-05:00"
    },
    {
      "id": 10,
      "title": "JellyTelly Jigsaw",
      "description": "Choose from several JellyTelly jigsaw puzzles or make your own.",
      "category": "Puzzles",
      "age": "All",
      "game_type": "Flash",
      "file_name": "jellytelly-jigsaw",
      "created_at": "2015-07-19T19:00:00.000-05:00",
      "updated_at": "2015-07-19T19:00:00.000-05:00"
    },
    {
      "id": 11,
      "title": "Jelly Swap",
      "description": "Arrange three or more jellies of the same color to clear them from the board.",
      "category": "Puzzles",
      "age": "5-8, 8+",
      "game_type": "Flash",
      "file_name": "jelly-swap",
      "created_at": "2015-07-19T19:00:00.000-05:00",
      "updated_at": "2015-07-19T19:00:00.000-05:00"
    },
    {
      "id": 12,
      "title": "Match Up",
      "description": "Test your memory and match the JellyTelly characters before time runs out.",
      "category": "Puzzles",
      "age": "All",
      "game_type": "Flash",
      "file_name": "matchup",
      "created_at": "2015-07-19T19:00:00.000-05:00",
      "updated_at": "2015-07-19T19:00:00.000-05:00"
    },
    {
      "id": 13,
      "title": "Spot the Difference",
      "description": "Find the differences in classic JellyTelly scenes before time runs out!",
      "category": "Puzzles",
      "age": "2-5, 5-8",
      "game_type": "Flash",
      "file_name": "difference",
      "created_at": "2015-07-19T19:00:00.000-05:00",
      "updated_at": "2015-07-19T19:00:00.000-05:00"
    },
    {
      "id": 14,
      "title": "Jelly Paint",
      "description": "Paint and print the JellyTelly Crew with your own crazy palette!",
      "category": "Create",
      "age": "2-5, 5-8",
      "game_type": "Flash",
      "file_name": "paint",
      "created_at": "2015-07-19T19:00:00.000-05:00",
      "updated_at": "2015-07-19T19:00:00.000-05:00"
    },
    {
      "id": 15,
      "title": "Puppet Producer",
      "description": "Create your own puppets with the JellyTelly Puppet Producer.",
      "category": "Create",
      "age": "2-5, 5-8",
      "game_type": "Flash",
      "file_name": "puppet-producer",
      "created_at": "2015-07-19T19:00:00.000-05:00",
      "updated_at": "2015-07-19T19:00:00.000-05:00"
    }
  ]
}
```

This endpoint returns list of games

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`GET /games HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`


## Get single game

```ruby

```

```shell
curl -X GET -H "Authorization: Token token="auth_token"" -H "Cache-Control: no-cache" 'http://api.jellytelly.com/games/15'
```

>The above command returns JSON structured like this:

```json
{  
   "games_info":[  
      {  
         "id":15,
         "title":"Puppet Producer",
         "description":"Create your own puppets with the JellyTelly Puppet Producer.",
         "category":"Create",
         "age":"2-5, 5-8",
         "game_type":"Flash",
         "file_name":"puppet-producer",
         "created_at":"2015-07-19T19:00:00.000-05:00",
         "updated_at":"2015-07-19T19:00:00.000-05:00"
      }
   ]
}
```

This endpoint returns specified game

<aside class="notice">NOTE: this method requires the auth_token</aside>

### HTTP Request

`GET /games/15 HTTP/1.1
Host: api.jellytelly.com
Authorization: Token token="auth_token"`

### URL Parameters

Parameter | Datatype | Description | Required?
--------- | ----------- | ----------- | -----------
id | String | Id of game | true
