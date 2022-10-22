## song/random

> Note: It is recommended to use `song/list` API as the local cache data source.

| arguments    | description                                | optional |
|:-------------|:-------------------------------------------|----------|
| start        | range of start (9+ => 9p , 10+ => 10p)     | true     |
| end          | range of end                               | true     |
| withsonginfo | boolean. if true, will reply with songinfo | true     |

###### Tag

* Enable Cors

#### ConvertFunction

```c#
var val = rating * 2 + (ratingPlus ? 1 : 0);
```

#### Example

+ `{apiurl}/botarcapi/song/random?start=19&end=22&withsonginfo=true`

###### Return data

```json5
{
  "status": 0,
  "content": {
    "id": "divinelight",
    "ratingClass": 2,
    "songinfo": {
      "name_en": "Divine Light of Myriad",
      "name_jp": "光速神授説 - Divine Light of Myriad -",
      "artist": "yoho",
      "bpm": "172",
      "bpm_base": 172.0,
      "set": "observer_append_2",
      "set_friendly": "Esoteric Order",
      "time": 142,
      "side": 0,
      "world_unlock": false,
      "remote_download": true,
      "bg": "observer_light",
      "date": 1626825602,
      "version": "3.7",
      "difficulty": 21,
      "rating": 108,
      "note": 1021,
      "chart_designer": "東星※神授",
      "jacket_designer": "緋原ヨウ",
      "jacket_override": false,
      "audio_override": false
    }
  }
}
```

