## assets/song

> Note: It is not recommended to use this API frequently.

| arguments  | description                                                        | optional                                                  |
|:-----------|:-------------------------------------------------------------------|-----------------------------------------------------------|
| song_name  | any song name for fuzzy querying                                   | true when songid or file is not null, otherwise false     |
| song_id    | sid in Arcaea songlist                                             | true when songname or file is not null, otherwise false   |
| difficulty | accept format are 3 or byn or beyond                               | true                                                      |
| file       | filename for special songs, such as stager_1 or melodyoflove_night | true when songid or songname is not null, otherwise false |

###### Tag

* Enable Cors

#### Example

+ `{apiurl}/arcapi/assets/song?file=stager_1`

###### Content-Type

```
image/jpeg
```