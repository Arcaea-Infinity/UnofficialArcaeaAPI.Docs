## assets/aff

> Note: It is not recommended to use this API frequently, and this API only returns affs from the installation package.

| arguments  | description                          | optional                                                  |
|:-----------|:-------------------------------------|-----------------------------------------------------------|
| song_name  | any song name for fuzzy querying     | true when songid or file is not null, otherwise false     |
| song_id    | sid in Arcaea songlist               | true when songname or file is not null, otherwise false   |
| difficulty | accept format are 3 or byn or beyond | true                                                      |

###### Tag

* Enable Cors

#### Example

+ `{apiurl}/arcapi/assets/aff?song_id=inkarusi&difficulty=2`

###### Content-Type

```
text/aff
```