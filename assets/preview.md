## assets/preview

> Note: It is not recommended to use this API frequently.

| arguments  | description                          | optional                                        |
|:-----------|:-------------------------------------|-------------------------------------------------|
| song_name  | any song name for fuzzy querying     | true when songid is not null, otherwise false   |
| song_id    | sid in Arcaea songlist               | true when songname is not null, otherwise false |
| difficulty | accept format are 3 or byn or beyond | true                                            |

###### Tag

* Enable Cors

* Need Token

#### Example

+ `{apiurl}/arcapi/assets/preview?song_id=ifi`

###### Content-Type

```
image/jpeg
```