## song/alias

| arguments  | description                                                                | optional                                        |
|:-----------|:---------------------------------------------------------------------------|-------------------------------------------------|
| songname   | any song name for fuzzy querying                                           | true when songid is not null, otherwise false   |
| songid     | sid in Arcaea songlist                                                     | true when songname is not null, otherwise false |

###### Tag

* Enable Cors

#### Example

+ `{apiurl}/botarcapi/song/alias?songid=ifi`

##### Return data

```json
{
    "status": 0,
    "content": [
        "色号",
        "对立色"
    ]
}
```
