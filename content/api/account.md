+++
title = "Account"
weight = 1
toc = true
+++

## Login

`/v1/account/login`

#### Parameters

|Name|Required|Type|
|---|---|---|
|tenant|Yes|string|
|username|Yes|string|
|password|Yes|string|

#### Example

Request: 

`pp:///v1/account/login?tenant=LABS&username=salesmand&password=1234`

Success:
```
{
  "result": {
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdWQiOiJQb3MiLCJleHAiOjE0O.z19pVl9OBV2RkGTOU2KIuLhLEJi6IS_Q9vxNjhYbjus",
    "userId": 1,
    "userName": "salesman",
    "roles": [
      {
        "name": "Salesman"
      }
    ],
    "tenantId": 1,
    "tenantCode": "LABS",
    "tenantName": "Labs",
    "spots": [
      {
        "id": 1,
        "code": "AC3E",
        "name": "天山店"
      }
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

`/v1/account/autologin`

#### Parameters

None

#### Example

Request:

`pp:///v1/account/autologin`

Success:

```
{
  "result": {
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdWQiOiJQb3MiLCJleHAiOjE0ODM5MzYxMDQsImh0dHA6Ly93d3cuYXNwbmV0Ym9pbGVycGxhdGUuY29tL2lkZW50aXR5L2NsYWltcy90ZW5hbnRJZCI6IjEiLCJpc3MiOiJMQUJTIiwibmFtZWlkIjoiMSIsIm5iZiI6MTQ4MzY3NjkwNCwicm9sZSI6IlNhbGVzbWFuIiwidW5pcXVlX25hbWUiOiJzYWxlc21hbiJ9.z19pVl9OBV2RkGTOU2KIuLhLEJi6IS_Q9vxNjhYbjus",
    "userId": 1,
    "userName": "salesman",
    "roles": [
      {
        "name": "Salesman"
      }
    ],
    "tenantId": 1,
    "tenantCode": "LABS",
    "tenantName": "Labs",
    "spots": [
      {
        "id": 1,
        "code": "AC3E",
        "name": "天山店"
      }
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
