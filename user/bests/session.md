## user/bests/session

| arguments  | description                                                     | optional                                        |
|:-----------|:----------------------------------------------------------------|-------------------------------------------------|
| user_name  | user name or 9-digit user code                                  | true when usercode is not null, otherwise false |
| user_code  | 9-digit user code                                               | true when user is not null, otherwise false     |

###### Tag

* Need Token

#### Example

+ `{apiurl}/arcapi/user/bests/session?user_name=ToasterKoishi`

###### Return data

```json5
{
  "status": 0,
  "content": {
    "session_info": "4@1a966fd8-3066-4935-975c-09cc1e042d7a"
  }
}
```

```json5
{
  "status": -33,
  "message": "duplicate bests requests within 12 hours. cached session generated",
  "content": {
    "session_info": "4@1a966fd8-3066-4935-975c-09cc1e042d7a"
  }
}
```