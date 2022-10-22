## user/best30

| arguments    | description                                                                     | optional                                        |
|:-------------|:--------------------------------------------------------------------------------|-------------------------------------------------|
| user         | user name or 9-digit user code                                                  | true when usercode is not null, otherwise false |
| usercode     | 9-digit user code                                                               | true when user is not null, otherwise false     |
| overflow     | number, range 0-10. The number of the	overflow records below the best30 minimum | true                                            |
| withrecent   | boolean. if true, will reply with recent_score                                  | true                                            |
| withsonginfo | boolean. if true, will reply with songinfo                                      | true                                            |

###### Tag

* Need Token

#### Example

+ `{apiurl}/botarcapi/user/best30?user=ToasterKoishi&withrecent=true&withsonginfo=true`

###### Return data (Edited for readability)

```json5
{
  "status": 0,
  "content": {
    "best30_avg": 12.707672500000001,
    "recent10_avg": 12.836982499999998,
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
    "best30_list": [
      {
        "score": 9956548,
        "health": 100,
        "rating": 13.082740000000001,
        "song_id": "grievouslady",
        "modifier": 0,
        "difficulty": 2,
        "clear_type": 1,
        "best_clear_type": 5,
        "time_played": 1614911430950,
        "near_count": 7,
        "miss_count": 3,
        "perfect_count": 1440,
        "shiny_perfect_count": 1376
      }
    ],
    "best30_songinfo": [
      {
        "name_en": "Grievous Lady",
        "name_jp": "",
        "artist": "Team Grimoire vs Laur",
        "bpm": "210",
        "bpm_base": 210.0,
        "set": "yugamu",
        "set_friendly": "Vicious Labyrinth",
        "time": 141,
        "side": 1,
        "world_unlock": false,
        "remote_download": true,
        "bg": "grievouslady",
        "date": 1509667208,
        "version": "1.5",
        "difficulty": 22,
        "rating": 113,
        "note": 1450,
        "chart_designer": "迷路深層",
        "jacket_designer": "シエラ",
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
