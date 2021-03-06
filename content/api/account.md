+++
title = "Account"
weight = 1
toc = true
+++

## Login

`/account/login`

#### Parameters

|Name|Required|Type|
|---|---|---|
|tenant|Yes|string|
|username|Yes|string|
|password|Yes|string|

#### Example

Request: 

`pp://staging/account/login?tenant=LABS&username=salesmand&password=1234`

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
    "result": null,
    "success": false,
    "error": {
        "code": 201,
        "message": "Login Failed.\nInvalid password."
    }
}
```

---

## Auto login

`/account/autologin`

#### Parameters

None

#### Example

Request:

`pp://staging/account/autologin`

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
  "result": null,
  "error": {
    "code": 202,
    "message": "Cannot get current user."
  }
}
```
---

<!--## Set Spot

`/account/set-spot`

#### Parameters

|Name|Required|Type|
|---|---|---|
|spotId|Yes|number|


#### Example

Request:

`pp://staging/account/set-spot?spotId=2`

Success:

```
{
  "result": {
    "token": "YOUR_TOKEN",
    "userId": 1000001,
    "userName": "saleswoman",
    "tenantId": 10,
    "tenantCode": "LABS",
    "tenantName": "LABS",
    "spots": [
      {
        "id": 2000001,
        "tenantId": 0,
        "name": "Event Hall",
        "contracts": [
          {
            "BrandCode": "Calvin Klein",
          },
          {
            "BrandCode": "Ted Baker",
          },
          {
            "BrandCode": "Lilly Pulitzer",
          }
        ]
      },
      {
        "id": 2000002,
        "tenantId": 0,
        "name": "天山店",
        "contracts": [
          {
            "BrandCode": "EE",
          },
          {
            "BrandCode": "EK",
          },
          {
            "BrandCode": "EA",
          }
        ]
      }
    ],
    "roles": [
      "salesman",
      "manager"
    ],
    "currentSpotId": 2000001
  },
  "success": true,
  "error": {}
}
```-->

---

## External Login

`/account/external-login`

#### Parameters

|Name|Required|Type|Desc|
|---|---|---|---|
|tenant|Yes|string| |
|token|Yes|string|JWT token|

- JWT token payload
  - brandCode
  - shopCode
- Secret
  - YOUR_TENANT_SCRET

#### Example

Request: 

`pp://staging/account/external-login?tenant=YOUR_TENANT_NAME&token=JWT_TOKEN`

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
  "result": null,
  "error": {
    "code": 201,
    "message": "Login Failed. Invalid token."
  }
}
```
