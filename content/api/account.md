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
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdWQiOiJQb3MiLCJleHAiOjE0ODg2NDA0MTMsImh0dHA6Ly93d3cuYXNwbmV0Ym9pbGVycGxhdGUuY29tL2lkZW50aXR5L2NsYWltcy90ZW5hbnRJZCI6IjEiLCJpc3MiOiJMQUJTIiwibmFtZWlkIjoiMSIsIm5iZiI6MTQ4ODM4MTIxMywicm9sZSI6IlNhbGVzbWFuLE1hbmFnZXIiLCJ1bmlxdWVfbmFtZSI6InNhbGVzbWFuIn0.sC9Qln1-AWgyled5Nj4MZ7tMsOuiLwqskDlAd2hs9vg",
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
            "code": "RC",
            "name": "Roem"
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
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdWQiOiJQb3MiLCJleHAiOjE0ODg2NDA0MTMsImh0dHA6Ly93d3cuYXNwbmV0Ym9pbGVycGxhdGUuY29tL2lkZW50aXR5L2NsYWltcy90ZW5hbnRJZCI6IjEiLCJpc3MiOiJMQUJTIiwibmFtZWlkIjoiMSIsIm5iZiI6MTQ4ODM4MTIxMywicm9sZSI6IlNhbGVzbWFuLE1hbmFnZXIiLCJ1bmlxdWVfbmFtZSI6InNhbGVzbWFuIn0.sC9Qln1-AWgyled5Nj4MZ7tMsOuiLwqskDlAd2hs9vg",
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
