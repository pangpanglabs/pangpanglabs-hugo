+++
title = "Cart"
weight = 4
toc = true
+++



## Create cart

`/cart/create-cart`

#### Parameters

None

#### Example

Request: 

`pp://staging/cart/create-cart`

Success:
```
{
  "result": {
    "id": 1,
    "items": null,
    "listPrice": 0,
    "salePrice": 0,
    "quantity": 0,
    "discount": 0,
    "customerInfo": null,
    "couponNo": "",
    "info": null,
    "userId": 1,
    "spotId": 2,
    "createdAt": "2017-03-01T15:28:49.136503665Z",
    "updatedAt": "2017-03-01T15:28:49.136503665Z"
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
    "code": 404,
    "message": "Cannot create cart."
  }
}
```

---


## Add item to cart

`/cart/add-item`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|number|
|uid|Yes|string|
|quantity|Yes|number|

#### Example

Request: 

`pp://staging/cart/add-item?cartId=1&uid=305228&quantity=2`

Success:
```
{
  "result": {
    "id": 1,
    "items": [
      {
        "uid": "305228",
        "name": "EKJP6CV102, (59)Navy, (135)135",
        "skuCode": "EKJP6CV10259135",
        "contentCode": "EKJP6CV102",
        "brandCode": "EK",
        "unitListPrice": 450,
        "unitSalePrice": 450,
        "quantity": 2,
        "listPrice": 900,
        "salePrice": 900,
        "discount": 0
      }
    ],
    "listPrice": 900,
    "salePrice": 900,
    "quantity": 2,
    "discount": 0,
    "customerInfo": null,
    "couponNo": "",
    "info": null,
    "userId": 1,
    "spotId": 2,
    "createdAt": "2017-03-01T15:28:49Z",
    "updatedAt": "2017-03-01T15:33:36.714647541Z"
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
    "code": 401,
    "message": "Cannot add item to current cart.\nCannot find product for 'skuId:12'"
  }
}
```

---


## Remove item from cart

`/cart/remove-item`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|number|
|skuId|Yes|number|
|quantity|Yes|number|

#### Example

Request: 

`pp://staging/cart/remove-item?cartId=1&uid=305228&quantity=1`

Success:
```
{
  "result": {
    "id": 1,
    "items": [
      {
        "uid": "305228",
        "name": "EKJP6CV102, (59)Navy, (135)135",
        "skuCode": "EKJP6CV10259135",
        "contentCode": "EKJP6CV102",
        "brandCode": "EK",
        "unitListPrice": 450,
        "unitSalePrice": 450,
        "quantity": 1,
        "listPrice": 450,
        "salePrice": 450,
        "discount": 0
      }
    ],
    "listPrice": 1350,
    "salePrice": 1350,
    "quantity": 1,
    "discount": 0,
    "customerInfo": null,
    "couponNo": "",
    "info": null,
    "userId": 1,
    "spotId": 2,
    "createdAt": "2017-03-01T15:28:49Z",
    "updatedAt": "2017-03-01T15:35:56.789085986Z"
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
    "code": 402,
    "message": "Cannot remove item from current cart.\nCannot find item for 'skuId:12' in current cart\n"
  }
}
```

---

## Set customer

`/cart/set-customer`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|number|
|no|Yes|string|

#### Example

Request: 

`pp://staging/cart/set-customer?cartId=1&no=RC10000000001`

Success:
```
{
  "result": {
    "id": 1,
    "items": [
      {
        "uid": "305228",
        "name": "EKJP6CV102, (59)Navy, (135)135",
        "skuCode": "EKJP6CV10259135",
        "contentCode": "EKJP6CV102",
        "brandCode": "EK",
        "unitListPrice": 450,
        "unitSalePrice": 450,
        "quantity": 1,
        "listPrice": 450,
        "salePrice": 450,
        "discount": 0
      }
    ],
    "listPrice": 1350,
    "salePrice": 1350,
    "quantity": 1,
    "discount": 0,
    "customerInfo": {
      "no": "10000000001",
      "brandCode": "RC",
      "mobile": "123456789021",
      "grade": 0,
      "cardType": "purpleCard",
      "mileage": {
        "currentPoints": 9000,
        "totalEarnPoints": 10000,
        "totalRedeemPoints": 10,
        "totalSaleAmount": "345.0"
      }
    },
    "couponNo": "",
    "info": null,
    "userId": 1,
    "spotId": 2,
    "createdAt": "2017-03-01T15:28:49Z",
    "updatedAt": "2017-03-01T15:39:08.371314559Z"
  },
  "success": true,
  "error": {}
}
```


## Set coupon

 
`/cart/set-coupon`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|number|
|no|Yes|string|

#### Example

Request: 

`pp://staging/cart/set-coupon?cartId=1&no=WA976CE9199756D5BC`

Success:
```
{
  "result": {
    "id": 1,
    "items": [
      {
        "uid": "305228",
        "name": "EKJP6CV102, (59)Navy, (135)135",
        "skuCode": "EKJP6CV10259135",
        "contentCode": "EKJP6CV102",
        "brandCode": "EK",
        "unitListPrice": 450,
        "unitSalePrice": 0,
        "quantity": 1,
        "listPrice": 450,
        "salePrice": 450,
        "discount": 0
      },
      {
        "uid": "1",
        "name": "LONG DOWN JUMPER, (39)Ivory, X-SMALL",
        "skuCode": "WHJP64T05C390XS",
        "contentCode": "WHJP64T05C",
        "brandCode": "WA",
        "unitListPrice": 1290,
        "unitSalePrice": 0,
        "quantity": 2,
        "listPrice": 2580,
        "salePrice": 1806,
        "discount": 774
      }
    ],
    "listPrice": 4380,
    "salePrice": 2256,
    "quantity": 3,
    "discount": 774,
    "customerInfo": {
      "no": "10000000001",
      "brandCode": "RC",
      "mobile": "123456789021",
      "grade": 0,
      "cardType": "purpleCard",
      "mileage": {
        "currentPoints": 9000,
        "totalEarnPoints": 10000,
        "totalRedeemPoints": 10,
        "totalSaleAmount": "345.0"
      }
    },
    "couponNo": "WA976CE9199756D5BC",
    "info": null,
    "userId": 1,
    "spotId": 2,
    "createdAt": "2017-03-01T15:28:49Z",
    "updatedAt": "2017-03-01T15:43:27.347863336Z"
  },
  "success": true,
  "error": {}
}
```


## Set info

 
`/cart/remove-cart`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|number|
|`key`|Yes|string|

#### Example

Request: 

`pp://staging/cart/set-info?cartId=1&payment[alipay]=150&payment[wxpay]=30&receipt=193018485875930103`

Success:
```
{
  "result": {
    "id": 1,
    "items": [
      {
        "uid": "305228",
        "name": "EKJP6CV102, (59)Navy, (135)135",
        "skuCode": "EKJP6CV10259135",
        "contentCode": "EKJP6CV102",
        "brandCode": "EK",
        "unitListPrice": 450,
        "unitSalePrice": 450,
        "quantity": 1,
        "listPrice": 450,
        "salePrice": 450,
        "discount": 0
      },
      {
        "uid": "1",
        "name": "LONG DOWN JUMPER, (39)Ivory, X-SMALL",
        "skuCode": "WHJP64T05C390XS",
        "contentCode": "WHJP64T05C",
        "brandCode": "WA",
        "unitListPrice": 1290,
        "unitSalePrice": 1290,
        "quantity": 2,
        "listPrice": 2580,
        "salePrice": 2580,
        "discount": 774
      }
    ],
    "listPrice": 7410,
    "salePrice": 5286,
    "quantity": 3,
    "discount": 2124,
    "customerInfo": {
      "no": "10000000001",
      "brandCode": "RC",
      "mobile": "123456789021",
      "grade": 0,
      "cardType": "purpleCard",
      "mileage": {
        "currentPoints": 9000,
        "totalEarnPoints": 10000,
        "totalRedeemPoints": 10,
        "totalSaleAmount": "345.0"
      }
    },
    "couponNo": "WA976CE9199756D5BC",
    "info": {
      "payment": {
        "alipay": "150",
        "wxpay": "30"
      },
      "receipt": "193018485875930103"
    },
    "userId": 1,
    "spotId": 2,
    "createdAt": "2017-03-01T15:28:49Z",
    "updatedAt": "2017-03-01T15:44:48.496016435Z"
  },
  "success": true,
  "error": {}
}
```

## Remove cart

 
`/cart/remove-cart`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|number|

#### Example

Request: 

`pp://staging/cart/remove-cart`

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
  "result": null,
  "error": {
    "code": 405,
    "message": "Cannot remove current cart."
  }
}
```

---


## Get all carts

`/cart/all-carts`

#### Parameters

None

#### Example

Request: 

`pp://staging/cart/all-carts`

Success:
```
{
  "result": [
    {
      "id": 1,
      "listPrice": 4380,
      "salePrice": 2256,
      "quantity": 3,
      "discount": 774,
      "customerInfo": {
        "no": "10000000001",
        "brandCode": "RC",
        "mobile": "123456789021",
        "grade": 0,
        "cardType": "purpleCard",
        "mileage": {
          "currentPoints": 9000,
          "totalEarnPoints": 10000,
          "totalRedeemPoints": 10,
          "totalSaleAmount": "345.0"
        }
      },
      "couponNo": "WA976CE9199756D5BC",
      "info": {
        "payment": {
          "alipay": "150",
          "wxpay": "30"
        },
        "receipt": "193018485875930103"
      },
      "userId": 1,
      "spotId": 2,
      "createdAt": "2017-03-01T15:28:49Z",
      "updatedAt": "2017-03-01T15:44:48Z"
    }
    {
      "id": 2,
      "listPrice": 1090,
      "salePrice": 1090,
      "quantity": 1,
      "discount": 0,
      "customerInfo": null,
      "couponNo": "",
      "info": null,
      "userId": 1,
      "spotId": 1,
      "createdAt": "2017-03-01T15:47:11Z",
      "updatedAt": "2017-03-01T15:47:22Z"
    }
  ],
  "success": true,
  "error": {}
}
```

---


## Get cart

 
`/cart/get-cart`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|number|

#### Example

Request: 

`pp://staging/cart/get-cart?cartId=1`

Success:
```
{
  "result": {
    "id": 1,
    "tenantId": "",
    "channel": "",
    "items": [
      {
        "uid": "305228",
        "name": "EKJP6CV102, (59)Navy, (135)135",
        "skuCode": "EKJP6CV10259135",
        "contentCode": "EKJP6CV102",
        "brandCode": "EK",
        "unitListPrice": 450,
        "unitSalePrice": 0,
        "quantity": 1,
        "listPrice": 450,
        "salePrice": 450,
        "discount": 0
      },
      {
        "uid": "1",
        "name": "LONG DOWN JUMPER, (39)Ivory, X-SMALL",
        "skuCode": "WHJP64T05C390XS",
        "contentCode": "WHJP64T05C",
        "brandCode": "WA",
        "unitListPrice": 1290,
        "unitSalePrice": 0,
        "quantity": 2,
        "listPrice": 2580,
        "salePrice": 1806,
        "discount": 774
      }
    ],
    "listPrice": 4380,
    "salePrice": 2256,
    "quantity": 3,
    "discount": 774,
    "customerInfo": {
      "no": "10000000001",
      "brandCode": "RC",
      "mobile": "123456789021",
      "grade": 0,
      "cardType": "purpleCard",
      "mileage": {
        "currentPoints": 9000,
        "totalEarnPoints": 10000,
        "totalRedeemPoints": 10,
        "totalSaleAmount": "345.0"
      }
    },
    "couponNo": "WA976CE9199756D5BC",
    "info": {
      "payment": {
        "alipay": "150",
        "wxpay": "30"
      },
      "receipt": "193018485875930103"
    },
    "userId": 1,
    "spotId": 2,
    "createdAt": "2017-03-01T15:28:49Z",
    "updatedAt": "2017-03-01T15:44:48Z"
  },
  "success": true,
  "error": {}
}
```