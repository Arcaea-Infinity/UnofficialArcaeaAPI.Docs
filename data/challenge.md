## data/challenge

> Note: It is designed for the release version of AUA, and not available for the release version.

| arguments | description         | optional                |
|:----------|:--------------------|-------------------------|
| path      | request arcapi path | false                   |
| body      | request body        | true when body is empty |
| time      | request timestamp   | true                    |

#### Allowed pathes

```json5
[
  "auth/login",
  "user",
  "user/me",
  "friend/me/delete",
  "friend/me/add",
  "score/song/friend",
  "purchase/me/stamina/fragment",
  "world/map/me"
]
```

###### Tag

* Need Token

#### Example

+ `{apiurl}/botarcapi/data/challenge?path=auth/login`

##### Return data (Edited for readability)

```json5
{
  "status": 0,
  "content": "JfdDAIQBAAAkdLOHw7PyRfWyhkJvH1Xzfevm7quQMwOk5Lc99fD1vgesJ8uf5ZJgPfgtYlYGDu1FLk31AaNAYfGocKoRMMSAlqDc4y/aZxXCn4cGjnJ7ovR9rkCQG8W1sJ9cHuK4CDo="
}
```
