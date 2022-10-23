# ArcaeaUnlimitedAPI

(or BotArcAPI CSharp implementation)

A fast and easy Arcaea API for your bot.

For the deploy tutorial of AUA, please refer to [How to deploy AUA](/deploy.md).

### Note

> Some APIs have an access limit of 10 requests per IP per day without a token.

### Community

> [Discord](https://discord.gg/4wSjfYpnY5)

### API Entry

+ [user/info](/user/info.md)
+ [user/best](/user/best.md)
+ [user/best30](/user/best30.md)


+ [song/info](/song/info.md)
+ [song/list](/song/list.md)
+ [song/alias](/song/alias.md)
+ [song/random](/song/random.md)


+ [assets/icon](/assets/icon.md)
+ [assets/char](/assets/char.md)
+ [assets/song](/assets/song.md)
+ [assets/preview](/assets/preview.md) [^1]


+ [data/update](/data/update.md)
+ [data/theory](/data/theory.md)
+ [data/playdata](/data/playdata.md)
+ [data/density](/data/density.md)
+ [data/challenge](/data/challenge.md) [^2]

[^1]: The `assets/preview` API is not available for release version of AUA. It is provided by [AffPreview](https://github.com/Arcaea-Infinity/Aff2Preview).

[^2]: The `data/challenge` API is not available for release version of AUA.

### Error status

| status | description                                               |
|:-------|:----------------------------------------------------------|
| -1     | invalid username or usercode                              |  
| -2     | invalid usercode                                          |  
| -3     | user not found                                            |  
| -4     | too many users                                            |  
| -5     | invalid songname or songid                                |  
| -6     | invalid songid                                            |  
| -7     | song not recorded                                         |  
| -8     | too many records                                          |  
| -9     | invalid difficulty                                        |  
| -10    | invalid recent/overflow number                            |  
| -11    | allocate an arc account failed                            |  
| -12    | clear friend failed                                       |  
| -13    | add friend failed                                         |  
| -14    | this song has no this level                               |  
| -15    | not played yet                                            |  
| -16    | user got shadowbanned                                     |
| -17    | querying best30 failed                                    |  
| -18    | update service unavailable                                |  
| -19    | invalid partner                                           |  
| -20    | file unavailable                                          |  
| -21    | invalid range                                             | 
| -22    | range of rating end smaller than its start                |
| -23    | potential is below the threshold of querying best30 (7.0) |  
| -24    | need to update arcaea, please contact maintainer          | 
| -25    | invalid version                                           | 
| -26    | daily query quota exceeded                                | 
| -27    | illegal hash, please contact maintainer                   |
| -233   | internal error occurred                                   |  

### Abnormal Example

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

