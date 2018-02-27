---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

toc_footers:
  
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

#Foreword

The basis for this documentation is the [CrowdTangle API Wiki](https://github.com/CrowdTangle/API/wiki) . I have migrated existing content into [Slate](https://github.com/lord/slate). I have created this to add a Slate implementation sample into my job portfolio. I am **_NOT_** the author of this document. 

#Introduction

You can use the CrowdTangle API to access posts, the leaderboard and the link-checker. Please contact your CrowdTangle representative for access. If you have access to the API, you can locate your API token via your dashboard under Settings > API Access. The CrowdTangle API is currently in a private beta, which means that while you can expect endpoints and parameters to remain stable, there will be other changes happening frequently.


# Authentication



```shell

# To authorize as a custom header:

curl "https://api.crowdtangle.com/posts"
  -H "x-api-token: your-api-token"
  
 # To authorize as a query parameter: 
 
curl "https://api.crowdtangle.com/posts?token=your-api-token"
```


> Make sure to replace `your-api-token` with your API token.

The CrowdTangle API expects the API token to be included either as a custom header with the name `x-api-token` or as a `token` query parameter. 

<aside class="notice">
You must replace <code>your-api-token</code> with your personal API token.
</aside>

# Making a request

All requests to the CrowdTangle API are made via GET to https://api.crowdtangle.com/. You must use https.

## GET /Posts


<!---
```shell
curl "http://example.com/api/kittens"
  -H "Authorization: meowmeowmeow"
```
--->


> JSON Structure:

```json
{
  "status": 200,
  "result": {
    "posts": [
      {
        "id": 1662400672,
        "platformId": "93625750491_10156590943270492",
        "platform": "Facebook",
        "date": "2016-02-09 15:00:00",
        "updated": "2016-03-01 02:04:41",
        "type": "photo",
        "message": "Happy Birthday to #Phillies Wall of Famer John Kruk!",
        "expandedLinks": [
          {
            "original": "https://www.facebook.com/Phillies/photos/a.188899285491.269976.93625750491/10156590943270492/?type=3",
            "expanded": "https://www.facebook.com/Phillies/photos/a.188899285491.269976.93625750491/10156590943270492/?type=3"
          }
        ],
        "link": "https://www.facebook.com/Phillies/photos/a.188899285491.269976.93625750491/10156590943270492/?type=3",
        "postUrl": "https://www.facebook.com/Phillies/posts/10156590943270492",
        "subscriberCount": 1684347,
        "score": 8.738522954091817,
        "media": [
          {
            "type": "photo",
            "url": "https://scontent.xx.fbcdn.net/hphotos-xfp1/v/t1.0-9/p720x720/12728987_10156590943270492_90073343638331316_n.jpg?oh=c7a16bfd8b41e13fdf54e62daa07795c&oe=576AD842",
            "height": 720,
            "width": 720,
            "full": "https://scontent.xx.fbcdn.net/hphotos-xfp1/v/t1.0-9/p720x720/12728987_10156590943270492_90073343638331316_n.jpg?oh=c7a16bfd8b41e13fdf54e62daa07795c&oe=576AD842"
          }
        ],
        "statistics": {
          "actual": {
            "likeCount": 11475,
            "shareCount": 1197,
            "commentCount": 465,
            "loveCount": 0,
            "wowCount": 0,
            "hahaCount": 0,
            "sadCount": 0,
            "angryCount": 0
          },
          "expected": {
            "likeCount": 1966,
            "shareCount": 160,
            "commentCount": 80,
            "loveCount": 0,
            "wowCount": 0,
            "hahaCount": 0,
            "sadCount": 0,
            "angryCount": 0
          }
        },
        "account": {
          "id": 992,
          "name": "Philadelphia Phillies",
          "handle": "Phillies",
          "profileImage": "https://scontent.xx.fbcdn.net/v/t1.0-1/p50x50/17554304_10158560861625492_845952810880537491_n.jpg?oh=79c8c102377f9cf19fafada807fcece4&oe=594D229D",
          "subscriberCount": 1703396,
          "url": "https://www.facebook.com/93625750491",
          "platform": "Facebook",
          "platformId": "93625750491",
          "verified": true
        }
      },
      {
        "id": 1420254373,
        "platformId": "19614945368_10153444965190369",
        "platform": "Facebook",
        "date": "2016-01-10 18:00:00",
        "date": "2017-04-13 03:02:50",
        "type": "native_video",
        "message": "My cats are always coming up with new, innovative ways to sit around.",
        "expandedLinks": [
          {
            "original": "https://www.facebook.com/TaylorSwift/videos/10153444965190369/",
            "expanded": "https://www.facebook.com/TaylorSwift/videos/10153444965190369/"
          }
        ],
        "link": "https://www.facebook.com/TaylorSwift/videos/10153444965190369/",
        "postUrl": "https://www.facebook.com/TaylorSwift/posts/10153444966305369",
        "subscriberCount": 73987186,
        "score": 1.9512645914396887,
        "media": [
          {
            "type": "video",
            "url": "https://video.xx.fbcdn.net/hvideo-xpf1/v/t42.1790-2/12554346_488798491321974_655798697_n.mp4?efg=eyJybHIiOjY5MywicmxhIjo1MTIsInZlbmNvZGVfdGFnIjoic3ZlX3NkIn0%3D&rl=693&vabr=385&oh=c4b0d0a140392ed1e70467ad873dcfc2&oe=5695EC62",
            "height": 0,
            "width": 0
          },
          {
            "type": "photo",
            "url": "https://scontent.xx.fbcdn.net/hvthumb-xpf1/v/t15.0-10/12474268_154354148269681_1401415196_n.jpg?oh=b115918988612d0127afb88fc9aacfbe&oe=5707855C",
            "height": 640,
            "width": 640,
            "full": "https://scontent.xx.fbcdn.net/hvthumb-xpf1/v/t15.0-10/12474268_154354148269681_1401415196_n.jpg?oh=b115918988612d0127afb88fc9aacfbe&oe=5707855C"
          }
        ],
        "statistics": {
          "actual": {
            "likeCount": 311401,
            "shareCount": 29805,
            "commentCount": 13871,
            "loveCount": 2225,
            "wowCount": 50,
            "hahaCount": 1168,
            "sadCount": 4,
            "angryCount": 10
          },
          "expected": {
            "likeCount": 141778,
            "shareCount": 4693,
            "commentCount": 3434,
            "loveCount": 13820,
            "wowCount": 609,
            "hahaCount": 239,
            "sadCount": 24,
            "angryCount": 49
          }
        },
        "account": {
          "id": 9083,
          "name": "Taylor Swift",
          "handle": "TaylorSwift",
          "profileImage": "https://scontent.xx.fbcdn.net/v/t1.0-1/p50x50/12998749_10153659625475369_5264917631114672817_n.jpg?oh=7675ec737f0b429cbf669b6584fe7ebe&oe=5985F4B9",
          "subscriberCount": 74585525,
          "url": "https://www.facebook.com/19614945368",
          "platform": "Facebook",
          "platformId": "19614945368",
          "verified": true
        }
      }
    ],
    "pagination": {
      "nextPage": "https://api.crowdtangle.com/posts?token=[your-token-here]&filterBy=overperforming&endDate=2016-02-13T00:41&startDate=2016-02-12T18:41:02&count=10&offset=10"
    }
  }
}
```

This endpoint retrieves a set of posts for the given parameters.

### Endpoint (HTTP Request)

`GET https://api.crowdtangle.com/posts`

### Query Parameters

Parameter | Default | Options | Description 
----------|---------|---------|-------------
count | `10` | `1-100` | The number of posts to return.
endDate | now | - | The latest date at which a post could be posted. Time zone is UTC. Format is “yyyy-mm-ddThh:mm:ss” or “yyyy-mm-dd” (defaults to time 00:00:00).
listIds | `null` (i.e. the entire dashboard) | - | The IDs of lists or saved searches to retrieve. These can be separated by commas to include multiple lists.
minInteractions | `0` | `> 0` | If set, will exclude posts with total interactions below this threshold.
offset | `0` | `> 0` | The number of posts to offset (generally used for pagination). Pagination links will also be provided in the response.
searchTerm | `null` | Any string | Returns only posts that match this search term. Terms AND automatically. Separate with commas for OR, use quotes for phrases. E.g. CrowdTangle API -> AND. CrowdTangle, API -> OR. "CrowdTangle API" -> AND in that exact order.
sortBy | `overperforming` | `date`, `interaction_rate`, `overperforming`, `total_interactions`, `underperforming` | The method by which to filter and order posts.
startDate | `null`| - | The earliest date at which a post could be posted. Time zone is UTC. Format is “yyyy-mm-ddThh:mm:ss” or “yyyy-mm-dd” (defaults to time 00:00:00). This must be before endDate. Timeframe and startDate are mutually exclusive; if both are passed, startDate will be preferred.
timeframe | `6 HOUR` | Any valid SQL interval (No, we don't pass it through to our database. Don't be silly) | The interval of time to consider from the endDate. Timeframe and startDate are mutually exclusive; if both are passed, startDate will be preferred. Depending on the number of posts, longer timeframes may not return within the timeout window. If you get a 504, try shortening your timeframe.
types | `null` (all) | `episode`, `extra_clip`, `link`, `live_video`, `live_video_complete`, `live_video_scheduled`, `native_video`, `photo`, `status`, `trailer`, `tweet`, `video`, `vine`, `youtube` | The types of post to include. These can be separated by commas to include multiple types. If you want all live videos (whether currently or formerly live), be sure to include both live_video and live_video_complete.
weightAngry, weightComment, weightHaha, weightLike, weightLoop, weightLove, weightRepost, weightRetweet, weightSad, weightShare, weightUpvote, weightView, weightWow | 0 | 0-10 | How much weight to give to each type of interaction. If you send in no weights, all weights will use the current dashboard defaults. If you send in at least one weight, all other weights will default to 0. Weights are multiplied by interaction counts: e.g. weightsComment at 1 and all others at 0 will find the most commented-on posts. weightsLike at 1 and weightsShare at 2 will give shares twice the impact as likes when computing scores.

<aside class="success">
The response contains both a status code and result. The result contains an array of post objects and pagination object with URL for the next and previous page. Refer to the JSON response.
</aside>

## GET /Posts/Search


> The API call returns a JSON structured like this:

```json
{
  "status": 200,
  "result": {
    "posts": [
      {
        "id": 2013897106,
        "platformId:" "8245623462_10153874455838463",
        "platform": "Facebook",
        "date": "2016-03-24 00:47:16",
        "updated": "2017-04-14 22:35:20",
        "type": "native_video",
        "message": "LeBron James with a monster first half of highlights for the Cleveland Cavaliers!",
        "expandedLinks": [
          {
            "original": "https://www.facebook.com/nba/videos/10153874455838463/",
            "expanded": "https://www.facebook.com/nba/videos/10153874455838463/"
          }
        ],
        "link": "https://www.facebook.com/nba/videos/10153874455838463/",
        "postUrl": "https://www.facebook.com/nba/posts/10153874455838463",
        "subscriberCount": 29215226,
        "score": 2.1423105540938283,
        "media": [
          {
            "type": "video",
            "url": "https://video.xx.fbcdn.net/hvideo-xpl1/v/t42.1790-2/12900635_575435455966516_2042072092_n.mp4?efg=eyJybHIiOjg1OCwicmxhIjo1ODMsInZlbmNvZGVfdGFnIjoic3ZlX3NkIn0%3D&rl=858&vabr=477&oh=9517d83ef9989d118408c1b40547a4c5&oe=56F5BE01",
            "height": 0,
            "width": 0
          },
          {
            "type": "photo",
            "url": "https://fb-s-b-a.akamaihd.net/h-ak-xft1/v/t15.0-10/s720x720/1067455_10153874459148463_1224669207_n.jpg?_nc_log=1&oh=5bc266c40ec589e72a57b24071e9a44b&oe=599922AE&__gda__=1501402904_1d6cde9fa2fd961836fb3d837c5e9f47",
            "height": 405,
            "width": 720,
            "full": "https://scontent.xx.fbcdn.net/hvthumb-xfp1/v/t15.0-10/s720x720/1067455_10153874459148463_1224669207_n.jpg?oh=9ee5128ce31229fde1a2afb313775581&oe=5796F9AE"
          }
        ],
        "statistics": {
          "actual": {
            "likeCount": 43511,
            "shareCount": 2913,
            "commentCount": 770,
            "loveCount": 542,
            "wowCount": 886,
            "hahaCount": 67,
            "sadCount": 5,
            "angryCount": 4
          },
          "expected": {
          "likeCount": 15442,
          "shareCount": 696,
          "commentCount": 261,
          "loveCount": 359,
          "wowCount": 296,
          "hahaCount": 35,
          "sadCount": 5,
          "angryCount": 5
          }
        },
        "account": {
          "id": 13509,
          "name": "NBA",
          "handle": "nba",
          "profileImage": "https://scontent.xx.fbcdn.net/v/t1.0-1/p50x50/14702298_10154466099813463_299662269705201551_n.jpg?oh=64e2c4cb2649e9596bf78faee8e1ff67&oe=59971989",
          "subscriberCount": 32956182,
          "url": "https://www.facebook.com/8245623462",
          "platform": "Facebook",
          "platformId": "8245623462",
          "verified": true
        }
      }
    ]
  }
}
```

This endpoint retrieves a set of posts for the given parameters and search terms. This endpoint, unlike the main `/posts` endpoint, searches the entire, cross-platform CrowdTangle system of posts. It can be limited by lists and accounts, but by default will search beyond the dashboard the token is associated with.

<aside class="warning">Access to the Search is restricted to a limited set customers and usage requires prior approval by CrowdTangle.</aside>

### Endpoint (HTTP Request)

`GET https://api.crowdtangle.com/posts/search`

### URL Parameters

Parameter | Default | Options | Description 
----------|---------|---------|-------------
and | `null` | - | An AND term that is added to the search query. For instance, if your `searchTerm` is 'lebron james, steph curry' and your `and` term is 'GOAT,' the posts must match ('lebron james' AND 'GOAT') OR ('steph curry' AND 'GOAT')
count | `10` | `1-100` | The number of posts to return.
endDate | now | - | The latest date at which a post could be posted. Time zone is UTC. Format is “yyyy-mm-ddThh:mm:ss” or “yyyy-mm-dd” (defaults to time 00:00:00).
inAccountIds | null | - |A comma-separated list of the IDs of accounts to search within. 
inListIds | null | - | A comma-separated list of the IDs of lists or saved searches to search within. 
minInteractions | `0` | `> 0` | If set, will exclude posts with total interactions below this threshold.
minSubscriberCount | `0` | `> 0` | The minimum number of subscribers an account must have to be included in the search results. 
not | `null` | - | A corollary to `and`, `not` will exclude all posts matching this word. 
notInAccountIds | null | - |A comma-separated list of the IDs of accounts to exclude. This behaves the same as notInListIds, except with specific accounts. 
notInListIds | null | - |  A comma-separated list of the the IDs of lists or saved searches to exclude from results. For instance, if don't want to see news outlet mentions of your search term, 'Lebron James,' you could exclude your sports publishers list.
notInTitle | `null` | - | Exclude all posts whose _account_ title matches this term. E.g. search for "CrowdTangle" but ignore any accounts that include the word "CrowdTangle" to see what other accounts are posting.
offset | `0` | `> 0` | The number of posts to offset (generally used for pagination). Pagination links will also be provided in the response.
platforms | `null` (i.e., all platforms) | facebook, instagram, reddit, twitter, vine | The platforms from which to retrieve posts. This value can be comma-separated.
searchTerm | `null` | Any string | Returns only posts that match this search term. Terms AND automatically. Separate with commas for OR, use quotes for phrases. E.g. CrowdTangle API -> AND. CrowdTangle, API -> OR. "CrowdTangle API" -> AND in that exact order.
sortBy | `overperforming` | `date`, `interaction_rate`, `overperforming`, `total_interactions`, `underperforming` | The method by which to filter and order posts.
startDate | `null`| - | The earliest date at which a post could be posted. Time zone is UTC. Format is “yyyy-mm-ddThh:mm:ss” or “yyyy-mm-dd” (defaults to time 00:00:00). This must be before endDate. Timeframe and startDate are mutually exclusive; if both are passed, startDate will be preferred.
timeframe | `6 HOUR` | Any valid SQL interval (No, we don't pass it through to our database. Don't be silly) | The interval of time to consider from the endDate. Timeframe and startDate are mutually exclusive; if both are passed, startDate will be preferred.
types | `null` (all) | `episode`, `extra_clip`, `link`, `live_video`, `live_video_complete`, `live_video_scheduled`, `native_video`, `photo`, `status`, `trailer`, `tweet`, `video`, `vine`, `youtube` | The types of post to include. These can be separated by commas to include multiple types. If you want all live videos (whether currently or formerly live), be sure to include both live_video and live_video_complete.
verifiedOnly | `false` | - | Limit results to verified accounts only. Note, this only applies to platforms that supply information about verified accounts. For instance, this will never return any posts on Vine.


## GET /lists


> The JSON response contains both a status code and a result. The status will always be `200` if there is no error:

```json
{
    status: 200,
    result: {
        lists: [{
            id: 1,
            title: "Best Star Wars Tweets",
            type: "SAVED_POSTS"
        },
        {
            id: 73914,
            title: "#r2d2",
            type: "SAVED_SEARCH"
        },
        {
            id: 74344,
            title: "Star Wars Characters",
            type: "LIST"
        }]
    }
}
```

This endpoint retrieves the lists, saved searches and saved post lists of the dashboard associated with the token sent in.

### Endpoint (HTTP Request)

`DELETE http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete

