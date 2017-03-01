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
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdWQiOiJQb3MiLCJleHAiOjE0ODg2NDA0MTMsImh0dHA6Ly93d3cuYXNwbmV0Ym9pbGVycGxhdGUuY29tL2lkZW50aXR5L2NsYWltcy90ZW5hbnRJZCI6IjEiLCJpc3MiOiJMQUJTIiwibmFtZWlkIjoiMSIsIm5iZiI6MTQ4ODM4MTIxMywicm9sZSI6IlNhbGVzbWFuLE1hbmFnZXIiLCJzcG90aWQiOiIyIiwidW5pcXVlX25hbWUiOiJzYWxlc21hbiJ9.02OrMulHTrwrwO_2-uDoQUhg1Ur31VRYcihurq5Id-0",
    "userId": 1,
    "userName": "salesman",
    "tenantId": 1,
    "tenantCode": "LABS",
    "tenantName": "Labs",
    "spots": [
      {
        "id": 1,
        "name": "天山店",
        "brands": [
          {
            "code": "WA",
            "name": "Paw in Paw"
          }
        ]
      },
      {
        "id": 2,
        "name": "上海正大广场",
        "brands": [
          {
            "code": "EK",
            "name": "Eland Kids"
          }
        ]
      }
    ],
    "roles": [
      "Salesman",
      "Manager"
    ],
    "currentSpotId": 2
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
        "allowOffline": true,
        "traceInterval": 10
      },
      "price": {
        "roundDigit": 2,
        "roundStrategy": "round",
        "currency": "CYN"
      }
    },
    "version": "0.0.2"
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