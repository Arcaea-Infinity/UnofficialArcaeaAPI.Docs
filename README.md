# ArcaeaUnlimitedAPI

(or BotArcAPI CSharp implementation)

A fast and easy Arcaea API for your bot.

For the deploy tutorial of AUA, please refer to [How to deploy AUA](/deploy.md).

### Note

> Some APIs have an access limit of 10 requests per IP per day without a token.

### Community

> [Discord](https://discord.gg/4wSjfYpnY5)

### API Entry

+ [user/info](/user/userinfo.md)
+ [user/best](/user/userbest.md)
+ [user/best30](/user/userbest30.md)


+ [song/info](/song/songinfo.md)
+ [song/list](/song/songlist.md)
+ [song/alias](/song/songalias.md)
+ [song/random](/song/songrandom.md)


+ [assets/icon](/assets/iconassets.md)
+ [assets/char](/assets/charassets.md)
+ [assets/song](/assets/songassets.md)


+ [data/update](/data/update.md)
+ [data/theory](/data/theory.md)
+ [data/playdata](/data/playdata.md)

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

### License

Licensed under `616 SB License`.

