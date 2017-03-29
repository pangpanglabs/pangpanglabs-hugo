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
    ]
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
    "message": "Login Failed. Invalid user name or password"
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
    ]
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

## Set Spot

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
```
