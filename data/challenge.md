## data/challenge

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

+ GET `{apiurl}/arcapi/data/challenge?path=auth/login`

+ POST `{apiurl}/arcapi/data/challenge?path=auth/login` with Json Array content

##### Return data (Edited for readability)

+ GET

```json5
{
  "status": 0,
  "content": "JfdDAIQBAAAkdLOHw7PyRfWyhkJvH1Xzfevm7quQMwOk5Lc99fD1vgesJ8uf5ZJgPfgtYlYGDu1FLk31AaNAYfGocKoRMMSAlqDc4y/aZxXCn4cGjnJ7ovR9rkCQG8W1sJ9cHuK4CDo="
}
```
