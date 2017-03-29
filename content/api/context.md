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
        "name": "Calvin Klein",
        "contracts": [
          {
            "BrandCode": "Calvin Klein",
            "ShopCode": "",
            "IsChief": false
          },
          {
            "BrandCode": "Ted Baker",
            "ShopCode": "",
            "IsChief": false
          },
          {
            "BrandCode": "Lilly Pulitzer",
            "ShopCode": "",
            "IsChief": false
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
            "ShopCode": "",
            "IsChief": false
          },
          {
            "BrandCode": "EK",
            "ShopCode": "",
            "IsChief": false
          },
          {
            "BrandCode": "EA",
            "ShopCode": "",
            "IsChief": false
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

`/context/settings`

#### Parameters

None

#### Example

Request:

`pp://staging/context/system`

Success:

```
{
  "result": {
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
    },
    "version": "0.0.3"
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