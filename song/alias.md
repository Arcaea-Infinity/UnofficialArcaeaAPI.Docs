## song/alias

> Note: It is recommended to use `song/list` API as the local cache data source.

| arguments  | description                                                                | optional                                        |
|:-----------|:---------------------------------------------------------------------------|-------------------------------------------------|
| songname   | any song name for fuzzy querying                                           | true when songid is not null, otherwise false   |
| songid     | sid in Arcaea songlist                                                     | true when songname is not null, otherwise false |

###### Tag

* Enable Cors

#### Example

+ `{apiurl}/botarcapi/song/alias?songid=ifi`

##### Return data

```json5
{
  "status": 0,
  "content": [
    "色号",
    "对立色"
  ]
}
```
