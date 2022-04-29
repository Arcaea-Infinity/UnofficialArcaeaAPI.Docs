## user/best

| arguments    | description                                                                | optional                                        |
|:-------------|:---------------------------------------------------------------------------|-------------------------------------------------|
| user         | user name or 9-digit user code                                             | true when usercode is not null, otherwise false |
| usercode     | 9-digit user code                                                          | true when user is not null, otherwise false     |
| songname     | any song name for fuzzy querying                                           | true when songid is not null, otherwise false   |
| songid       | sid in Arcaea songlist                                                     | true when songname is not null, otherwise false |
| difficulty   | accept format are 0/1/2/3 or pst/prs/ftr/byn or past/present/future/beyond | false                                           |
| withrecent   | boolean. if true, will reply with recent_score                             | true                                            |
| withsonginfo | boolean. if true, will reply with songinfo                                 | true                                            |

###### Tag

* User-Agent Needed

#### Example

+ `{apiurl}/botarcapi/user/best?user=ToasterKoishi&songid=ifi&difficulty=ftr&withrecent=true&withsonginfo=true`

###### Return data

```json
{
  "status": 0,
  "content": {
    "account_info": {
      "code": "062596721",
      "name": "ToasterKoishi",
      "user_id": 4,
      "is_mutual": false,
      "is_char_uncapped_override": false,
      "is_char_uncapped": true,
      "is_skill_sealed": false,
      "rating": 1274,
      "join_date": 1487816563340,
      "character": 12
    },
    "record": {
      "score": 9979257,
      "health": 100,
      "rating": 2.9862849999999996,
      "song_id": "ifi",
      "modifier": 0,
      "difficulty": 2,
      "clear_type": 1,
      "best_clear_type": 5,
      "time_played": 1598919831344,
      "near_count": 5,
      "miss_count": 1,
      "perfect_count": 1570,
      "shiny_perfect_count": 1466
    },
    "songinfo": [
      {
        "name_en": "#1f1e33",
        "name_jp": "",
        "artist": "かめりあ(EDP)",
        "bpm": "181",
        "bpm_base": 181.0,
        "set": "vs",
        "set_friendly": "Black Fate",
        "time": 163,
        "side": 1,
        "world_unlock": false,
        "remote_download": true,
        "bg": "vs_conflict",
        "date": 1590537604,
        "version": "3.0",
        "difficulty": 21,
        "rating": 109,
        "note": 1576,
        "chart_designer": "夜浪 VS 東星 \"Convergence\"",
        "jacket_designer": "望月けい",
        "jacket_override": false,
        "audio_override": false
      }
    ],
    "recent_score": {
      "user_id": 4,
      "score": 9982099,
      "health": 100,
      "rating": 11.510494999999999,
      "song_id": "espebranch",
      "modifier": 0,
      "difficulty": 2,
      "clear_type": 2,
      "best_clear_type": 3,
      "time_played": 1651045525836,
      "near_count": 4,
      "miss_count": 0,
      "perfect_count": 1054,
      "shiny_perfect_count": 1003
    },
    "recent_songinfo": {
      "name_en": "LunarOrbit -believe in the Espebranch road-",
      "name_jp": "白道、多希望羊と信じありく。",
      "artist": "Apo11o program ft. 大瀬良あい",
      "bpm": "192",
      "bpm_base": 192.0,
      "set": "base",
      "set_friendly": "Arcaea",
      "time": 141,
      "side": 1,
      "world_unlock": true,
      "remote_download": false,
      "bg": "mirai_conflict",
      "date": 1535673600,
      "version": "1.7",
      "difficulty": 18,
      "rating": 96,
      "note": 1058,
      "chart_designer": "月刊Toaster",
      "jacket_designer": "hideo",
      "jacket_override": false,
      "audio_override": false
    }
  }
}
```

