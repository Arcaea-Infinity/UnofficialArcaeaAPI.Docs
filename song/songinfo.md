## song/info

| arguments  | description                                                                | optional                                        |
|:-----------|:---------------------------------------------------------------------------|-------------------------------------------------|
| songname   | any song name for fuzzy querying                                           | true when songid is not null, otherwise false   |
| songid     | sid in Arcaea songlist                                                     | true when songname is not null, otherwise false |

###### Tag

* Enable Cors

#### Example

+ `{apiurl}/botarcapi/song/info?songname=infinity`

###### Return data

```json
{
  "status": 0,
  "content": {
    "song_id": "infinityheaven",
    "difficulties": [
      {
        "name_en": "Infinity Heaven",
        "name_jp": "",
        "artist": "HyuN",
        "bpm": "160",
        "bpm_base": 160.0,
        "set": "base",
        "set_friendly": "Arcaea",
        "time": 154,
        "side": 0,
        "world_unlock": false,
        "remote_download": false,
        "bg": "",
        "date": 1491868800,
        "version": "1.0",
        "difficulty": 2,
        "rating": 15,
        "note": 336,
        "chart_designer": "Nitro",
        "jacket_designer": "Tagtraume",
        "jacket_override": false,
        "audio_override": false
      },
      {
        "name_en": "Infinity Heaven",
        "name_jp": "",
        "artist": "HyuN",
        "bpm": "160",
        "bpm_base": 160.0,
        "set": "base",
        "set_friendly": "Arcaea",
        "time": 154,
        "side": 0,
        "world_unlock": false,
        "remote_download": false,
        "bg": "",
        "date": 1491868800,
        "version": "1.0",
        "difficulty": 10,
        "rating": 55,
        "note": 545,
        "chart_designer": "Nitro",
        "jacket_designer": "Tagtraume",
        "jacket_override": false,
        "audio_override": false
      },
      {
        "name_en": "Infinity Heaven",
        "name_jp": "",
        "artist": "HyuN",
        "bpm": "160",
        "bpm_base": 160.0,
        "set": "base",
        "set_friendly": "Arcaea",
        "time": 154,
        "side": 0,
        "world_unlock": false,
        "remote_download": false,
        "bg": "",
        "date": 1491868800,
        "version": "1.0",
        "difficulty": 14,
        "rating": 75,
        "note": 853,
        "chart_designer": "Nitro",
        "jacket_designer": "Tagtraume",
        "jacket_override": false,
        "audio_override": false
      },
      {
        "name_en": "Infinity Heaven",
        "name_jp": "",
        "artist": "HyuN",
        "bpm": "160",
        "bpm_base": 160.0,
        "set": "base",
        "set_friendly": "Arcaea",
        "time": 154,
        "side": 0,
        "world_unlock": false,
        "remote_download": false,
        "bg": "",
        "date": 1590537602,
        "version": "3.0",
        "difficulty": 18,
        "rating": 96,
        "note": 986,
        "chart_designer": "Nitr∞",
        "jacket_designer": "Tagtraume",
        "jacket_override": true,
        "audio_override": false
      }
    ],
    "alias": [
      "无限天堂",
      "无尽天堂"
    ]
  }
}
```

