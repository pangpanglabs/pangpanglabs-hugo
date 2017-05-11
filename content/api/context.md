+++
title = "Context"
weight = 2
toc = true
+++

## Get current user

`/context/user`

#### Parameters

None

#### Example

Request:

`pp://staging/context/user`

Success:

```
{
    "result": {
        "userId": 11,
        "userName": "HANGUANG-EE-C30R",
        "tenantId": 5,
        "tenantCode": "HANGUANG",
        "tenantName": "HANGUANG",
        "spots": [
            {
                "id": 26,
                "channelId": 12,
                "code": "EE-C30R",
                "name": "EE 北京中友",
                "colleagues": [
                    {
                        "userId": 19,
                        "username": "7000056022",
                        "displayName": "李桥秀"
                    },
                    {
                        "userId": 17,
                        "username": "7000041934",
                        "displayName": "康小伐"
                    },
                    {
                        "userId": 12,
                        "username": "6000079545",
                        "displayName": "武凯"
                    }
                ]
            }
        ],
        "roles": [
            "salesman"
        ],
        "currentSpotId": 26,
        "currentChannelId": 12
    },
    "success": true,
    "error": {}
}
```

Fail:

```
{
  "success": false,
  "error": {
    "code": 202,
    "message": "Cannot get current user."
  }
}
```

---


## Get system information

`/context/system`

#### Parameters

None

#### Example

Request:

`pp://staging/context/system`

Success:

```
{
    "result": {
        "version": "0.0.6",
        "setting": {
            "system": {
                "allowOffline": false,
                "traceInterval": 10
            },
            "price": {
                "roundDigit": 2,
                "roundStrategy": "round",
                "currency": "CYN"
            }
        }        
    },
    "success": true,
    "error": {}
}
```

Fail:

```
{
  "success": false,
  "error": {
    "code": 202,
    "message": "Cannot get settings."
  }
}
```