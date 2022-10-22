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

* Need Token

#### Example

+ `{apiurl}/botarcapi/user/best?user=ToasterKoishi&songid=ifi&difficulty=ftr&withrecent=true&withsonginfo=true`

###### Return data

```json5
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
      "rating": 12.796285000000001,
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
        "set_friendly": "BlackFate",
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
        "chart_designer": "夜浪VS東星\"Convergence\"",
        "jacket_designer": "望月けい",
        "jacket_override": false,
        "audio_override": false
      }
    ],
    "recent_score": {
      "user_id": 4,
      "score": 9992128,
      "health": 100,
      "rating": 11.76064,
      "song_id": "macromod",
      "modifier": 2,
      "difficulty": 2,
      "clear_type": 2,
      "best_clear_type": 2,
      "time_played": 1651198101733,
      "near_count": 2,
      "miss_count": 0,
      "perfect_count": 1115,
      "shiny_perfect_count": 1081
    },
    "recent_songinfo": {
      "name_en": "MacrocosmicModulation",
      "name_jp": "",
      "artist": "JAKAZiD",
      "bpm": "170",
      "bpm_base": 170.0,
      "set": "single",
      "set_friendly": "MemoryArchive",
      "time": 147,
      "side": 0,
      "world_unlock": false,
      "remote_download": true,
      "bg": "single2_light",
      "date": 1645056004,
      "version": "3.12",
      "difficulty": 19,
      "rating": 98,
      "note": 1117,
      "chart_designer": "Exschwas↕on",
      "jacket_designer": "装甲枕",
      "jacket_override": false,
      "audio_override": false
    }
  }
}
```

