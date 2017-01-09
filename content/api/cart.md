+++
title = "Cart"
weight = 4
toc = true
+++



## Create cart

`/v1/cart/create-cart`

#### Parameters

None

#### Example

Request: 

`pp:///v1/cart/create-cart`

Success:
```
{
  "result": {
    "id": 1,
    "tenantId": "",
    "items": [],
    "subTotal": 0,
    "total": 0,
    "quantity": 0,
    "userId": 1,
    "createdAt": "2017-01-06T04:56:51.667893692Z",
    "updatedAt": "2017-01-06T04:56:51.667893692Z"
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
    "code": 404,
    "message": "Cannot create cart."
  }
}
```

---


## Add item to cart

`/v1/cart/add-item`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|number|
|skuId|Yes|number|
|quantity|Yes|number|

#### Example

Request: 

`pp:///v1/cart/add-item?cartId=1&skuId=12&quantity=2`

Success:
```
{
  "result": {
    "id": 1,
    "tenantId": "",
    "items": [
      {
        "skuId": 12,
        "contentId": 12,
        "skuCode": "SF_PRO_11_1",
        "name": "Sound Forge Pro 11 (recurring)",
        "quantity": 2,
        "unitPrice": 54.99,
        "price": 54.99,
        "total": 109.98
      }
    ],
    "subTotal": 109.98,
    "total": 109.98,
    "quantity": 2,
    "userId": 1,
    "createdAt": "2017-01-06T04:56:51.667893692Z",
    "updatedAt": "2017-01-06T04:58:53.669251111Z"
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
    "code": 401,
    "message": "Cannot add item to current cart.\nCannot find product for 'skuId:12'"
  }
}
```

---


## Remove item from cart

`/v1/cart/remove-item`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|number|
|skuId|Yes|number|
|quantity|Yes|number|

#### Example

Request: 

`pp:///v1/cart/remove-item?cartId=1&skuId=12&quantity=1`

Success:
```
{
  "result": {
    "id": 1,
    "tenantId": "",
    "items": [
      {
        "skuId": 12,
        "contentId": 12,
        "skuCode": "SF_PRO_11_1",
        "name": "Sound Forge Pro 11 (recurring)",
        "quantity": 1,
        "unitPrice": 54.99,
        "price": 54.99,
        "total": 54.99
      }
    ],
    "subTotal": 54.99,
    "total": 54.99,
    "quantity": 1,
    "userId": 1,
    "createdAt": "2017-01-06T04:56:51.667893692Z",
    "updatedAt": "2017-01-06T05:00:03.212766277Z"
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
    "code": 402,
    "message": "Cannot remove item from current cart.\nCannot find item for 'skuId:12' in current cart\n"
  }
}
```

---


## Remove cart

 
`/v1/cart/remove-cart`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|number|

#### Example

Request: 

`pp:///v1/cart/remove-cart`

Success:
```
{
  "success": true,
  "result": null,
  "error": {}
}
```

Fail:

```
{
  "success": false,
  "error": {
    "code": 405,
    "message": "Cannot remove current cart."
  }
}
```

---


## Get all carts

`/v1/cart/all-carts`

#### Parameters

None

#### Example

Request: 

`pp:///v1/cart/all-carts`

Success:
```
{
  "result": [
    {
      "id": 2,
      "items": [
        {
          "skuId": 12,
          "contentId": 12,
          "skuCode": "SF_PRO_11_1",
          "name": "Sound Forge Pro 11 (recurring)",
          "quantity": 1,
          "unitPrice": 54.99,
          "price": 54.99,
          "total": 54.99
        }
      ],
      "subTotal": 54.99,
      "total": 54.99,
      "quantity": 1,
      "userId": 1,
      "createdAt": "2017-01-06T04:56:51.667893692Z",
      "updatedAt": "2017-01-06T05:00:03.212766277Z"
    },
    {
      "id": 3,
      "items": [
        {
          "skuId": 12,
          "contentId": 12,
          "skuCode": "SF_PRO_11_1",
          "name": "Sound Forge Pro 11 (recurring)",
          "quantity": 1,
          "unitPrice": 54.99,
          "price": 54.99,
          "total": 54.99
        }
      ],
      "subTotal": 54.99,
      "total": 54.99,
      "quantity": 1,
      "userId": 1,
      "createdAt": "2017-01-08T13:01:48.545481616Z",
      "updatedAt": "2017-01-08T13:01:48.545481616Z"
    }
  ],
  "success": true,
  "error": {}
}
```

---


## Get cart

 
`/v1/cart/get-cart`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|number|

#### Example

Request: 

`pp:///v1/cart/get-cart?cartId=2`

Success:
```
{
  "success": true,
  "result": {
    "id": 2,
    "items": [
      {
        "skuId": 12,
        "contentId": 12,
        "skuCode": "SF_PRO_11_1",
        "name": "Sound Forge Pro 11 (recurring)",
        "quantity": 1,
        "unitPrice": 54.99,
        "price": 54.99,
        "total": 54.99
      }
    ],
    "subTotal": 54.99,
    "total": 54.99,
    "quantity": 1,
    "userId": 1,
    "createdAt": "2017-01-06T04:56:51.667893692Z",
    "updatedAt": "2017-01-06T05:00:03.212766277Z"
  },
  "error": {}
}
```