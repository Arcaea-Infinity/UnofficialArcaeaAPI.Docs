## assets/preview

> Note: It is not recommended to use this API frequently.

| arguments  | description                          | optional                                        |
|:-----------|:-------------------------------------|-------------------------------------------------|
| songname   | any song name for fuzzy querying     | true when songid is not null, otherwise false   |
| songid     | sid in Arcaea songlist               | true when songname is not null, otherwise false |
| difficulty | accept format are 3 or byn or beyond | true                                            |

###### Tag

* Enable Cors

* Need Token

#### Example

+ `{apiurl}/botarcapi/assets/preview?songid=ifi`

###### Content-Type

```
image/png
```