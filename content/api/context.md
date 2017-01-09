+++
title = "Context"
weight = 2
toc = true
+++

## Get current user

`/v1/context/user`

#### Parameters

None

#### Example

Request:

`pp:///v1/context/user`

Success:

```
{
  "result": {    
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
  "error": {
    "code": 202,
    "message": "Cannot get current user."
  }
}
```

---


## Get system settings

`/v1/context/settings`

#### Parameters

None

#### Example

Request:

`pp:///v1/context/settings`

Success:

```
{
  "result": {
    "tenantId": 1,
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