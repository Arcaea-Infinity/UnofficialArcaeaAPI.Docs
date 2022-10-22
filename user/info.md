## user/info

| arguments    | description                                                     | optional                                        |
|:-------------|:----------------------------------------------------------------|-------------------------------------------------|
| user         | user name or 9-digit user code                                  | true when usercode is not null, otherwise false |
| usercode     | 9-digit user code                                               | true when user is not null, otherwise false     |
| recent       | number, range 0-7. The number of recently played songs expected | true                                            |
| withsonginfo | boolean. if true, will reply with songinfo                      | true                                            |

###### Tag

* Need Token

#### Example

+ `{apiurl}/botarcapi/user/info?user=ToasterKoishi&recent=2&withsonginfo=true`

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
    "recent_score": [
      {
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
      {
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
      }
    ],
    "songinfo": [
      {
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
      },
      {
        "name_en": "LunarOrbit-believeintheEspebranchroad-",
        "name_jp": "白道、多希望羊と信じありく。",
        "artist": "Apo11oprogramft.大瀬良あい",
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
    ]
  }
}
```
