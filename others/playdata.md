## playdata

| arguments  | description                          | optional                                                |
|:-----------|:-------------------------------------|---------------------------------------------------------|
| songname   | any song name for fuzzy querying     | true when songid or file is not null, otherwise false   |
| songid     | sid in Arcaea songlist               | true when songname or file is not null, otherwise false |
| difficulty | accept format are 3 or byn or beyond | true                                                    |
| start      | range of potential start (100*)      | false                                                   |
| end        | range of potential end  (100*)       | false                                                   |

###### Tag

* Enable Cors

#### Example

+ `{apiurl}/botarcapi/playdata?songid=ifi&difficulty=2&start=1280&end=1288`

##### Return data

```json
{
  "status": 0,
  "content": [
    {
      "fscore": 1000,
      "count": 125
    },
    {
      "fscore": 999,
      "count": 28
    },
    {
      "fscore": 998,
      "count": 26
    },
    {
      "fscore": 997,
      "count": 19
    },
    {
      "fscore": 996,
      "count": 14
    },
    {
      "fscore": 995,
      "count": 6
    },
    {
      "fscore": 994,
      "count": 2
    }
  ]
}
```
