## user/info

| arguments    | description                                                     | optional                                        |
|:-------------|:----------------------------------------------------------------|-------------------------------------------------|
| user         | user name or 9-digit user code                                  | true when usercode is not null, otherwise false |
| usercode     | 9-digit user code                                               | true when user is not null, otherwise false     |
| recent       | number, range 0-7. The number of recently played songs expected | true                                            |
| withsonginfo | boolean. if true, will reply with songinfo                      | true                                            |

###### Tag

* User-Agent Needed

#### Example

+ `{apiurl}/botarcapi/user/info?user=ToasterKoishi&recent=2&withsonginfo=true`

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
    "recent_score": [
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
      },
      {
        "score": 9877383,
        "health": 100,
        "rating": 11.886915,
        "song_id": "seclusion",
        "modifier": 2,
        "difficulty": 2,
        "clear_type": 5,
        "best_clear_type": 5,
        "time_played": 1650581540921,
        "near_count": 8,
        "miss_count": 10,
        "perfect_count": 1114,
        "shiny_perfect_count": 1058
      }
    ],
    "songinfo": [
      {
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
      },
      {
        "name_en": "Seclusion",
        "name_jp": "",
        "artist": "Laur feat. Sennzai",
        "bpm": "175",
        "bpm_base": 175.0,
        "set": "observer",
        "set_friendly": "Esoteric Order",
        "time": 138,
        "side": 1,
        "world_unlock": true,
        "remote_download": true,
        "bg": "observer_conflict",
        "date": 1626825603,
        "version": "3.7",
        "difficulty": 20,
        "rating": 105,
        "note": 1132,
        "chart_designer": "N•Ex•T",
        "jacket_designer": "海鵜げそ",
        "jacket_override": false,
        "audio_override": false
      }
    ]
  }
}
```
