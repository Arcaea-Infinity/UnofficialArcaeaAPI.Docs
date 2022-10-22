## data/density

> Note: It is a large data set, so it is not recommended to use this API frequently.

| arguments  | description                          | optional                                                |
|:-----------|:-------------------------------------|---------------------------------------------------------|
| songname   | any song name for fuzzy querying     | true when songid or file is not null, otherwise false   |
| songid     | sid in Arcaea songlist               | true when songname or file is not null, otherwise false |
| difficulty | accept format are 3 or byn or beyond | true                                                    |

###### Tag

* Enable Cors

#### Example

+ `{apiurl}/botarcapi/data/density?songid=ifi&difficulty=2`

##### Return data (Edited for readability)

```json5
{
  "status": 0,
  "content": [
    [
      1000, // fscore, (score/10000)
      115, // fpotential (potential/10)
      1 // count
    ],
    [
      1000,
      116,
      1
    ],
    [
      1000,
      117,
      1
    ]
  ]
}
```
