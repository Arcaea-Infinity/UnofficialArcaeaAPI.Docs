# UnofficialArcaeaAPI

A slow Arcaea API for my own use.

### Note

> Some APIs will be inaccessible without a token. [^1]

### API Entry

+ [user/info](/user/info.md)
+ [user/best](/user/best.md)
+ [user/bests/session](/user/bests/session.md)
+ [user/bests/result](/user/bests/result.md)


+ [song/info](/song/info.md)
+ [song/list](/song/list.md)
+ [song/alias](/song/alias.md)
+ [song/random](/song/random.md)


+ [assets/icon](/assets/icon.md)
+ [assets/char](/assets/char.md)
+ [assets/song](/assets/song.md)
+ [assets/aff](/assets/aff.md)
+ [assets/preview](/assets/preview.md) [^2]


+ [data/update](/data/update.md)
+ [data/theory](/data/theory.md)
+ [data/challenge](/data/challenge.md)
+ [data/cert](/data/cert.md)


+ [image/user/*](/image/user.md)  [^3]


[^1]: For functions of the API those are requiring token: Please send header with `Authorization` and the value `Bearer token_here`.

[^2]: The `assets/preview` API is provided by [AffPreview](https://github.com/Arcaea-Infinity/Aff2Preview).

[^3]: The `image/user/bests/session` API is not available.

### Error status

| status | description                                                            |
|:-------|:-----------------------------------------------------------------------|
| -1     | invalid username or usercode                                           |  
| -2     | invalid usercode                                                       |  
| -3     | user not found                                                         |  
| -4     | too many users                                                         |  
| -5     | invalid songname or songid                                             |  
| -6     | invalid songid                                                         |  
| -7     | song not recorded                                                      |  
| -8     | too many records (*)                                                   |  
| -9     | invalid difficulty                                                     |  
| -10    | invalid recent/overflow number                                         |  
| -11    | allocate an arc account failed                                         |  
| -12    | clear friend failed                                                    |  
| -13    | add friend failed                                                      |  
| -14    | this song has no this level                                            |  
| -15    | not played yet                                                         |  
| -16    | user got shadowbanned                                                  |
| -17    | querying bests failed                                                  |  
| -18    | update service unavailable                                             |  
| -19    | invalid partner                                                        |  
| -20    | file unavailable                                                       |  
| -21    | invalid range                                                          | 
| -22    | range of rating end smaller than its start                             |
| -23    | potential is below the threshold of querying bests (10.0)              |  
| -24    | need to update arcaea, please contact maintainer                       | 
| -25    | invalid version                                                        | 
| -26    | daily query quota exceeded                                             | 
| -27    | illegal hash, please contact maintainer                                |
| -28    | image server error                                                     |
| -29    | invalid session info                                                   |
| -30    | session expired                                                        |
| -31    | session querying, queried charts: ${queriedCharts} (*)                 |
| -32    | session waiting for account, account count: ${accountCount} (*)        |
| -33    | duplicate bests requests within 12 hours. cached session generated (*) |
| -34    | invalid account                                                        |
| -233   | internal error occurred                                                |  

> (*) means return additional data

#### Abnormal Example

+ `{apiurl}/botarcapi/song/alias?songid=gl`

+ ##### Return data

```json
{
    "status": -5,
    "message": "invalid songname or songid"
}
```

specially,

+ `{apiurl}/botarcapi/song/info?songname=lc`

+ ##### Return data

```json
{
  "status": -8,
  "message": "too many records",
  "content": {
    "songs": [
      "lostcivilization",
      "lastcelebration"
    ]
  }
}
```

### Credits

 + Special thanks to [TheSnowfield](https://github.com/TheSnowfield) for her [BotArcAPI](https://github.com/Arcaea-Infinity/BotArcAPIs-Memories) project and the extremely important assistance support in the development.

 + Special thanks to [tiger0132](https://github.com/tiger0132) for his [ArcUpdAPI](https://github.com/Arcaea-Infinity/ArcUpdAPI) project and for giving me permission to use his code.

 + Special thanks to [InariAimu](https://github.com/InariAimu) and [Linwenxuan04](https://github.com/Linwenxuan04) for [Aff2Preview](https://github.com/Arcaea-Infinity/Aff2Preview) project.

 + Special thanks to all those who contributed to this project or made suggestions.

### License

Licensed under `616 SB License`.

