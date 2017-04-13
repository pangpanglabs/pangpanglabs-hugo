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
    "id": 1349,
    "tenantId": 12,
    "listPrice": 0,
    "salePrice": 0,
    "quantity": 0,
    "discount": 0,
    "remainAmount": 0,
    "mileage": {
      "current": 0,
      "available": 0,
      "use": 0
    },
    "customerInfo": null,
    "couponInfo": null,
    "info": null,
    "payments": null,
    "userId": 1000001,
    "spotId": 2000001,
    "createdAt": "2017-03-29T07:47:02.773134948Z",
    "updatedAt": "0001-01-01T00:00:00Z",
    "items": null,
    "suggests": null
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

`pp://staging/cart/add-item?cartId=1349&skuId=184184&quantity=2`

Success:
```
{
  "result": {
    "id": 1349,
    "tenantId": 12,
    "listPrice": 1694,
    "salePrice": 1498,
    "quantity": 3,
    "discount": 196,
    "remainAmount": 1498,
    "customerInfo": null,
    "mileage": {
      "current": 0,
      "available": 0,
      "use": 0
    },
    "couponInfo": null,
    "info": null,
    "payments": null,
    "userId": 1000002,
    "spotId": 2000001,
    "createdAt": "2017-04-13T15:50:41Z",
    "updatedAt": "2017-04-13T16:03:30.373911583Z",
    "items": [
      {
        "sku": {
          "id": 184184,
          "contentId": 15579,
          "name": "EERA72505B, (30)Yellow, (160)160",
          "code": "EERA72505B30160",
          "listPrice": 498,
          "salePrice": 498,
          "discountName": "",
          "brandCode": "EE",
          "contentCode": "EE",
          "images": {
              "large": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL.jpg",
                  "width": 385,
                  "height": 500
              },
              "medium": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL160_.jpg",
                  "width": 123,
                  "height": 160
              },
              "small": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL75_.jpg",
                  "width": 58,
                  "height": 75
              }
          },
          "options": [
            {
              "k": "Size",
              "v": "(160)160"
            },
            {
              "k": "Color",
              "v": "(30)Yellow"
            }
          ]
        },
        "quantity": 1,
        "listPrice": 498,
        "salePrice": 498,
        "discount": 0
      },
      {
        "sku": {
          "id": 184413,
          "contentId": 15621,
          "name": "EETA72553N, (59)Navy, (155)155",
          "code": "EETA72553N59155",
          "listPrice": 598,
          "salePrice": 500,
          "discountName": "EETA72553N Discount! ￥500",
          "brandCode": "EE",
          "contentCode": "EE",
          "images": {
              "large": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL.jpg",
                  "width": 385,
                  "height": 500
              },
              "medium": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL160_.jpg",
                  "width": 123,
                  "height": 160
              },
              "small": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL75_.jpg",
                  "width": 58,
                  "height": 75
              }
          },
          "options": [
            {
              "k": "Size",
              "v": "(155)155"
            },
            {
              "k": "Color",
              "v": "(59)Navy"
            }
          ]
        },
        "quantity": 2,
        "listPrice": 1196,
        "salePrice": 1000,
        "discount": 196
      }
    ],
    "suggests": [
      {
        "name": "EERA72505 Bundle Sale",
        "desc": "",
        "listPrice": 796,
        "salePrice": 600,
        "startAt": "2017-04-13T11:32:47Z",
        "endAt": "2017-05-13T11:32:47Z",
        "channelId": 0,
        "virtualContents": [
          {
            "contentId": 15579,
            "listPrice": 498,
            "salePrice": 400
          },
          {
            "contentId": 15628,
            "listPrice": 298,
            "salePrice": 200
          }
        ]
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

`pp://staging/cart/remove-item?cartId=1349&skuId=184184&quantity=1`

Success:
```
{
  "result": {
    "id": 1349,
    "tenantId": 12,
    "listPrice": 1096,
    "salePrice": 998,
    "quantity": 2,
    "discount": 98,
    "remainAmount": 998,
    "customerInfo": null,
    "mileage": {
      "current": 0,
      "available": 0,
      "use": 0
    },
    "couponInfo": null,
    "info": null,
    "payments": null,
    "userId": 1000002,
    "spotId": 2000001,
    "createdAt": "2017-04-13T15:50:41Z",
    "updatedAt": "2017-04-13T16:00:48.401563037Z",
    "items": [
      {
        "sku": {
          "id": 184184,
          "contentId": 15579,
          "name": "EERA72505B, (30)Yellow, (160)160",
          "code": "EERA72505B30160",
          "listPrice": 498,
          "salePrice": 498,
          "discountName": "",
          "brandCode": "EE",
          "contentCode": "EE",
          "images": {
              "large": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL.jpg",
                  "width": 385,
                  "height": 500
              },
              "medium": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL160_.jpg",
                  "width": 123,
                  "height": 160
              },
              "small": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL75_.jpg",
                  "width": 58,
                  "height": 75
              }
          },
          "options": [
            {
              "k": "Size",
              "v": "(160)160"
            },
            {
              "k": "Color",
              "v": "(30)Yellow"
            }
          ]
        },
        "quantity": 1,
        "listPrice": 498,
        "salePrice": 498,
        "discount": 0
      },
      {
        "sku": {
          "id": 184413,
          "contentId": 15621,
          "name": "EETA72553N, (59)Navy, (155)155",
          "code": "EETA72553N59155",
          "listPrice": 598,
          "salePrice": 500,
          "discountName": "EETA72553N Discount! ￥500",
          "brandCode": "EE",
          "contentCode": "EE",
          "images": {
              "large": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL.jpg",
                  "width": 385,
                  "height": 500
              },
              "medium": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL160_.jpg",
                  "width": 123,
                  "height": 160
              },
              "small": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL75_.jpg",
                  "width": 58,
                  "height": 75
              }
          },
          "options": [
            {
              "k": "Size",
              "v": "(155)155"
            },
            {
              "k": "Color",
              "v": "(59)Navy"
            }
          ]
        },
        "quantity": 1,
        "listPrice": 598,
        "salePrice": 500,
        "discount": 98
      }
    ],
    "suggests": [
      {
        "name": "EERA72505 Bundle Sale",
        "desc": "",
        "listPrice": 796,
        "salePrice": 600,
        "startAt": "2017-04-13T11:32:47Z",
        "endAt": "2017-05-13T11:32:47Z",
        "channelId": 0,
        "virtualContents": [
          {
            "contentId": 15579,
            "listPrice": 498,
            "salePrice": 400
          },
          {
            "contentId": 15628,
            "listPrice": 298,
            "salePrice": 200
          }
        ]
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

`pp://staging/cart/set-customer?cartId=1349&no=EE0000053147`

Success:
```
{
  "result": {
    "id": 1349,
    "tenantId": 12,
    "listPrice": 1096,
    "salePrice": 998,
    "quantity": 2,
    "discount": 98,
    "remainAmount": 998,
    "customerInfo": {
      "id": 1065586,
      "no": "0000053147",
      "brandCode": "EE",
      "mobile": "13818448893",
      "grade": 3,
      "cardType": "diamondCard",
      "mileage": {
        "currentPoints": 208,
        "totalEarnPoints": 1108,
        "totalRedeemPoints": 900,
        "totalSaleAmount": 36330.94
      },
      "benefit": {
        "mileage": 208,
        "max_mileage_percent": 50,
        "discount_percent": 5,
        "max_discount_price": 0,
        "birthday_discount_percent": 30,
        "max_birthday_price": 5000
      }
    },
    "mileage": {
      "current": 208,
      "available": 208,
      "use": 0
    },
    "couponInfo": null,
    "info": null,
    "payments": null,
    "userId": 1000002,
    "spotId": 2000001,
    "createdAt": "2017-04-13T15:50:41Z",
    "updatedAt": "2017-04-13T16:00:48.401563037Z",
    "items": [
      {
        "sku": {
          "id": 184184,
          "contentId": 15579,
          "name": "EERA72505B, (30)Yellow, (160)160",
          "code": "EERA72505B30160",
          "listPrice": 498,
          "salePrice": 498,
          "discountName": "",
          "brandCode": "EE",
          "contentCode": "EE",
          "images": {
              "large": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL.jpg",
                  "width": 385,
                  "height": 500
              },
              "medium": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL160_.jpg",
                  "width": 123,
                  "height": 160
              },
              "small": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL75_.jpg",
                  "width": 58,
                  "height": 75
              }
          },
          "options": [
            {
              "k": "Size",
              "v": "(160)160"
            },
            {
              "k": "Color",
              "v": "(30)Yellow"
            }
          ]
        },
        "quantity": 1,
        "listPrice": 498,
        "salePrice": 498,
        "discount": 0
      },
      {
        "sku": {
          "id": 184413,
          "contentId": 15621,
          "name": "EETA72553N, (59)Navy, (155)155",
          "code": "EETA72553N59155",
          "listPrice": 598,
          "salePrice": 500,
          "discountName": "EETA72553N Discount! ￥500",
          "brandCode": "EE",
          "contentCode": "EE",
          "images": {
              "large": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL.jpg",
                  "width": 385,
                  "height": 500
              },
              "medium": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL160_.jpg",
                  "width": 123,
                  "height": 160
              },
              "small": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL75_.jpg",
                  "width": 58,
                  "height": 75
              }
          },
          "options": [
            {
              "k": "Size",
              "v": "(155)155"
            },
            {
              "k": "Color",
              "v": "(59)Navy"
            }
          ]
        },
        "quantity": 1,
        "listPrice": 598,
        "salePrice": 500,
        "discount": 98
      }
    ],
    "suggests": [
      {
        "name": "EERA72505 Bundle Sale",
        "desc": "",
        "listPrice": 796,
        "salePrice": 600,
        "startAt": "2017-04-13T11:32:47Z",
        "endAt": "2017-05-13T11:32:47Z",
        "channelId": 0,
        "virtualContents": [
          {
            "contentId": 15579,
            "listPrice": 498,
            "salePrice": 400
          },
          {
            "contentId": 15628,
            "listPrice": 298,
            "salePrice": 200
          }
        ]
      }
    ]
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

`pp://staging/cart/set-coupon?cartId=1349&no=EE4EEDE03E762A2AA2`

Success:
```
{
  "result": {
    "id": 1349,
    "tenantId": 12,
    "listPrice": 1096,
    "salePrice": 898,
    "quantity": 2,
    "discount": 198,
    "remainAmount": 898,
    "customerInfo": {
      "id": 1065586,
      "no": "0000053147",
      "brandCode": "EE",
      "mobile": "13818448893",
      "grade": 3,
      "cardType": "diamondCard",
      "mileage": {
        "currentPoints": 208,
        "totalEarnPoints": 1108,
        "totalRedeemPoints": 900,
        "totalSaleAmount": 36330.94
      },
      "benefit": {
        "mileage": 208,
        "max_mileage_percent": 50,
        "discount_percent": 5,
        "max_discount_price": 0,
        "birthday_discount_percent": 30,
        "max_birthday_price": 5000
      }
    },
    "mileage": {
      "current": 208,
      "available": 208,
      "use": 0
    },
    "couponInfo": {
      "no": "EE4EEDE03E762A2AA2",
      "couponType": "Discount",
      "discountName": "8折优惠",
      "eventId": "EE2017030024"
    },
    "info": null,
    "payments": null,
    "userId": 1000002,
    "spotId": 2000001,
    "createdAt": "2017-04-13T15:50:41Z",
    "updatedAt": "2017-04-13T16:00:48.401563037Z",
    "items": [
      {
        "sku": {
          "id": 184184,
          "contentId": 15579,
          "name": "EERA72505B, (30)Yellow, (160)160",
          "code": "EERA72505B30160",
          "listPrice": 498,
          "salePrice": 398,
          "discountName": "8折优惠",
          "brandCode": "EE",
          "contentCode": "EE",
          "images": {
              "large": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL.jpg",
                  "width": 385,
                  "height": 500
              },
              "medium": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL160_.jpg",
                  "width": 123,
                  "height": 160
              },
              "small": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL75_.jpg",
                  "width": 58,
                  "height": 75
              }
          },
          "options": [
            {
              "k": "Size",
              "v": "(160)160"
            },
            {
              "k": "Color",
              "v": "(30)Yellow"
            }
          ]
        },
        "quantity": 1,
        "listPrice": 498,
        "salePrice": 398,
        "discount": 100
      },
      {
        "sku": {
          "id": 184413,
          "contentId": 15621,
          "name": "EETA72553N, (59)Navy, (155)155",
          "code": "EETA72553N59155",
          "listPrice": 598,
          "salePrice": 500,
          "discountName": "EETA72553N Discount! ￥500",
          "brandCode": "EE",
          "contentCode": "EE",
          "images": {
              "large": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL.jpg",
                  "width": 385,
                  "height": 500
              },
              "medium": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL160_.jpg",
                  "width": 123,
                  "height": 160
              },
              "small": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL75_.jpg",
                  "width": 58,
                  "height": 75
              }
          },
          "options": [
            {
              "k": "Size",
              "v": "(155)155"
            },
            {
              "k": "Color",
              "v": "(59)Navy"
            }
          ]
        },
        "quantity": 1,
        "listPrice": 598,
        "salePrice": 500,
        "discount": 98
      }
    ],
    "suggests": [
      {
        "name": "EERA72505 Bundle Sale",
        "desc": "",
        "listPrice": 796,
        "salePrice": 600,
        "startAt": "2017-04-13T11:32:47Z",
        "endAt": "2017-05-13T11:32:47Z",
        "channelId": 0,
        "virtualContents": [
          {
            "contentId": 15579,
            "listPrice": 498,
            "salePrice": 400
          },
          {
            "contentId": 15628,
            "listPrice": 298,
            "salePrice": 200
          }
        ]
      }
    ]
  },
  "success": true,
  "error": {}
}
```


## Set info

 
`/cart/set-info`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|number|
|`key`|Yes|string|

#### Example

Request: 

`pp://staging/cart/set-info?cartId=326&receipt=193018485875930103&casher=nancy`

Success:
```
{
  "result": {
    "id": 1349,
    "tenantId": 12,
    "listPrice": 1096,
    "salePrice": 898,
    "quantity": 2,
    "discount": 198,
    "remainAmount": 898,
    "customerInfo": {
      "id": 1065586,
      "no": "0000053147",
      "brandCode": "EE",
      "mobile": "13818448893",
      "grade": 3,
      "cardType": "diamondCard",
      "mileage": {
        "currentPoints": 208,
        "totalEarnPoints": 1108,
        "totalRedeemPoints": 900,
        "totalSaleAmount": 36330.94
      },
      "benefit": {
        "mileage": 208,
        "max_mileage_percent": 50,
        "discount_percent": 5,
        "max_discount_price": 0,
        "birthday_discount_percent": 30,
        "max_birthday_price": 5000
      }
    },
    "mileage": {
      "current": 208,
      "available": 208,
      "use": 0
    },
    "couponInfo": {
      "no": "EE4EEDE03E762A2AA2",
      "couponType": "Discount",
      "discountName": "8折优惠",
      "eventId": "EE2017030024"
    },
    "info": {
      "receipt": "193018485875930103",
      "casher": "nancy"
    },
    "payments": null,
    "userId": 1000002,
    "spotId": 2000001,
    "createdAt": "2017-04-13T15:50:41Z",
    "updatedAt": "2017-04-13T16:00:48.401563037Z",
    "items": [
      {
        "sku": {
          "id": 184184,
          "contentId": 15579,
          "name": "EERA72505B, (30)Yellow, (160)160",
          "code": "EERA72505B30160",
          "listPrice": 498,
          "salePrice": 398,
          "discountName": "8折优惠",
          "brandCode": "EE",
          "contentCode": "EE",
          "images": {
              "large": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL.jpg",
                  "width": 385,
                  "height": 500
              },
              "medium": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL160_.jpg",
                  "width": 123,
                  "height": 160
              },
              "small": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL75_.jpg",
                  "width": 58,
                  "height": 75
              }
          },
          "options": [
            {
              "k": "Size",
              "v": "(160)160"
            },
            {
              "k": "Color",
              "v": "(30)Yellow"
            }
          ]
        },
        "quantity": 1,
        "listPrice": 498,
        "salePrice": 398,
        "discount": 100
      },
      {
        "sku": {
          "id": 184413,
          "contentId": 15621,
          "name": "EETA72553N, (59)Navy, (155)155",
          "code": "EETA72553N59155",
          "listPrice": 598,
          "salePrice": 500,
          "discountName": "EETA72553N Discount! ￥500",
          "brandCode": "EE",
          "contentCode": "EE",
          "images": {
              "large": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL.jpg",
                  "width": 385,
                  "height": 500
              },
              "medium": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL160_.jpg",
                  "width": 123,
                  "height": 160
              },
              "small": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL75_.jpg",
                  "width": 58,
                  "height": 75
              }
          },
          "options": [
            {
              "k": "Size",
              "v": "(155)155"
            },
            {
              "k": "Color",
              "v": "(59)Navy"
            }
          ]
        },
        "quantity": 1,
        "listPrice": 598,
        "salePrice": 500,
        "discount": 98
      }
    ],
    "suggests": [
      {
        "name": "EERA72505 Bundle Sale",
        "desc": "",
        "listPrice": 796,
        "salePrice": 600,
        "startAt": "2017-04-13T11:32:47Z",
        "endAt": "2017-05-13T11:32:47Z",
        "channelId": 0,
        "virtualContents": [
          {
            "contentId": 15579,
            "listPrice": 498,
            "salePrice": 400
          },
          {
            "contentId": 15628,
            "listPrice": 298,
            "salePrice": 200
          }
        ]
      }
    ]
  },
  "success": true,
  "error": {}
}
```

## Use mileage

`/cart/use-mileage`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|number|
|amount|Yes|number|

#### Example

Request: 

`pp://staging/cart/use-mileage?cartId=1349&amount=208`

Success:
```
{
  "result": {
    "id": 1349,
    "tenantId": 12,
    "listPrice": 1096,
    "salePrice": 898,
    "quantity": 2,
    "discount": 198,
    "remainAmount": 690,
    "customerInfo": {
      "id": 1065586,
      "no": "0000053147",
      "brandCode": "EE",
      "mobile": "13818448893",
      "grade": 3,
      "cardType": "diamondCard",
      "mileage": {
        "currentPoints": 208,
        "totalEarnPoints": 1108,
        "totalRedeemPoints": 900,
        "totalSaleAmount": 36330.94
      },
      "benefit": {
        "mileage": 208,
        "max_mileage_percent": 50,
        "discount_percent": 5,
        "max_discount_price": 0,
        "birthday_discount_percent": 30,
        "max_birthday_price": 5000
      }
    },
    "mileage": {
      "current": 208,
      "available": 208,
      "use": 208
    },
    "couponInfo": {
      "no": "EE4EEDE03E762A2AA2",
      "couponType": "Discount",
      "discountName": "8折优惠",
      "eventId": "EE2017030024"
    },
    "info": {
      "receipt": "193018485875930103",
      "casher": "nancy"
    },
    "payments": null,
    "userId": 1000002,
    "spotId": 2000001,
    "createdAt": "2017-04-13T15:50:41Z",
    "updatedAt": "2017-04-13T16:00:48.401563037Z",
    "items": [
      {
        "sku": {
          "id": 184184,
          "contentId": 15579,
          "name": "EERA72505B, (30)Yellow, (160)160",
          "code": "EERA72505B30160",
          "listPrice": 498,
          "salePrice": 398,
          "discountName": "8折优惠",
          "brandCode": "EE",
          "contentCode": "EE",
          "images": {
              "large": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL.jpg",
                  "width": 385,
                  "height": 500
              },
              "medium": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL160_.jpg",
                  "width": 123,
                  "height": 160
              },
              "small": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL75_.jpg",
                  "width": 58,
                  "height": 75
              }
          },
          "options": [
            {
              "k": "Size",
              "v": "(160)160"
            },
            {
              "k": "Color",
              "v": "(30)Yellow"
            }
          ]
        },
        "quantity": 1,
        "listPrice": 498,
        "salePrice": 398,
        "discount": 100
      },
      {
        "sku": {
          "id": 184413,
          "contentId": 15621,
          "name": "EETA72553N, (59)Navy, (155)155",
          "code": "EETA72553N59155",
          "listPrice": 598,
          "salePrice": 500,
          "discountName": "EETA72553N Discount! ￥500",
          "brandCode": "EE",
          "contentCode": "EE",
          "images": {
              "large": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL.jpg",
                  "width": 385,
                  "height": 500
              },
              "medium": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL160_.jpg",
                  "width": 123,
                  "height": 160
              },
              "small": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL75_.jpg",
                  "width": 58,
                  "height": 75
              }
          },
          "options": [
            {
              "k": "Size",
              "v": "(155)155"
            },
            {
              "k": "Color",
              "v": "(59)Navy"
            }
          ]
        },
        "quantity": 1,
        "listPrice": 598,
        "salePrice": 500,
        "discount": 98
      }
    ],
    "suggests": [
      {
        "name": "EERA72505 Bundle Sale",
        "desc": "",
        "listPrice": 796,
        "salePrice": 600,
        "startAt": "2017-04-13T11:32:47Z",
        "endAt": "2017-05-13T11:32:47Z",
        "channelId": 0,
        "virtualContents": [
          {
            "contentId": 15579,
            "listPrice": 498,
            "salePrice": 400
          },
          {
            "contentId": 15628,
            "listPrice": 298,
            "salePrice": 200
          }
        ]
      }
    ]
  },
  "success": true,
  "error": {}
}
```

## Set payment

 
`/cart/set-payment`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|number|
|method|Yes|string|
|amount|Yes|number|

#### Example

Request: 

`pp://staging/cart/set-payment?cartId=1349&method=alipay&amount=690`

Success:
```
{
  "result": {
    "id": 1349,
    "tenantId": 12,
    "listPrice": 1096,
    "salePrice": 898,
    "quantity": 2,
    "discount": 198,
    "remainAmount": 0,
    "customerInfo": {
      "id": 1065586,
      "no": "0000053147",
      "brandCode": "EE",
      "mobile": "13818448893",
      "grade": 3,
      "cardType": "diamondCard",
      "mileage": {
        "currentPoints": 208,
        "totalEarnPoints": 1108,
        "totalRedeemPoints": 900,
        "totalSaleAmount": 36330.94
      },
      "benefit": {
        "mileage": 208,
        "max_mileage_percent": 50,
        "discount_percent": 5,
        "max_discount_price": 0,
        "birthday_discount_percent": 30,
        "max_birthday_price": 5000
      }
    },
    "mileage": {
      "current": 208,
      "available": 208,
      "use": 208
    },
    "couponInfo": {
      "no": "EE4EEDE03E762A2AA2",
      "couponType": "Discount",
      "discountName": "8折优惠",
      "eventId": "EE2017030024"
    },
    "info": {
      "receipt": "193018485875930103",
      "casher": "nancy"
    },
    "payments": [
      {
        "method": "alipay",
        "amount": 690
      }
    ],
    "userId": 1000002,
    "spotId": 2000001,
    "createdAt": "2017-04-13T15:50:41Z",
    "updatedAt": "2017-04-13T16:00:48.401563037Z",
    "items": [
      {
        "sku": {
          "id": 184184,
          "contentId": 15579,
          "name": "EERA72505B, (30)Yellow, (160)160",
          "code": "EERA72505B30160",
          "listPrice": 498,
          "salePrice": 398,
          "discountName": "8折优惠",
          "brandCode": "EE",
          "contentCode": "EE",
          "images": {
              "large": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL.jpg",
                  "width": 385,
                  "height": 500
              },
              "medium": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL160_.jpg",
                  "width": 123,
                  "height": 160
              },
              "small": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL75_.jpg",
                  "width": 58,
                  "height": 75
              }
          },
          "options": [
            {
              "k": "Size",
              "v": "(160)160"
            },
            {
              "k": "Color",
              "v": "(30)Yellow"
            }
          ]
        },
        "quantity": 1,
        "listPrice": 498,
        "salePrice": 398,
        "discount": 100
      },
      {
        "sku": {
          "id": 184413,
          "contentId": 15621,
          "name": "EETA72553N, (59)Navy, (155)155",
          "code": "EETA72553N59155",
          "listPrice": 598,
          "salePrice": 500,
          "discountName": "EETA72553N Discount! ￥500",
          "brandCode": "EE",
          "contentCode": "EE",
          "images": {
              "large": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL.jpg",
                  "width": 385,
                  "height": 500
              },
              "medium": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL160_.jpg",
                  "width": 123,
                  "height": 160
              },
              "small": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL75_.jpg",
                  "width": 58,
                  "height": 75
              }
          },
          "options": [
            {
              "k": "Size",
              "v": "(155)155"
            },
            {
              "k": "Color",
              "v": "(59)Navy"
            }
          ]
        },
        "quantity": 1,
        "listPrice": 598,
        "salePrice": 500,
        "discount": 98
      }
    ],
    "suggests": [
      {
        "name": "EERA72505 Bundle Sale",
        "desc": "",
        "listPrice": 796,
        "salePrice": 600,
        "startAt": "2017-04-13T11:32:47Z",
        "endAt": "2017-05-13T11:32:47Z",
        "channelId": 0,
        "virtualContents": [
          {
            "contentId": 15579,
            "listPrice": 498,
            "salePrice": 400
          },
          {
            "contentId": 15628,
            "listPrice": 298,
            "salePrice": 200
          }
        ]
      }
    ]
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

`pp://staging/cart/remove-cart?cartId=1349`

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
      "id": 347,
      "tenantId": 12,
      "listPrice": 148,
      "salePrice": 148,
      "quantity": 1,
      "discount": 0,
      "remainAmount": 148,
      "customerInfo": null,
      "mileage": {
        "current": 0,
        "available": 0,
        "use": 0
      },
      "couponInfo": null,
      "info": null,
      "payments": null,
      "userId": 1000002,
      "spotId": 2000001,
      "createdAt": "2017-03-29T16:10:45Z",
      "updatedAt": "0001-01-01T00:00:00Z",
      "items": null,
      "suggests": null
    },
    {
      "id": 352,
      "tenantId": 12,
      "listPrice": 0,
      "salePrice": 0,
      "quantity": 0,
      "discount": 0,
      "remainAmount": 0,
      "customerInfo": null,
      "mileage": {
        "current": 0,
        "available": 0,
        "use": 0
      },
      "couponInfo": null,
      "info": null,
      "payments": null,
      "userId": 1000002,
      "spotId": 2000001,
      "createdAt": "2017-03-29T16:31:33Z",
      "updatedAt": "0001-01-01T00:00:00Z",
      "items": null,
      "suggests": null
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

`pp://staging/cart/get-cart?cartId=1349`

Success:
```
{
  "result": {
    "id": 1349,
    "tenantId": 12,
    "listPrice": 1096,
    "salePrice": 898,
    "quantity": 2,
    "discount": 198,
    "remainAmount": 0,
    "customerInfo": {
      "id": 1065586,
      "no": "0000053147",
      "brandCode": "EE",
      "mobile": "13818448893",
      "grade": 3,
      "cardType": "diamondCard",
      "mileage": {
        "currentPoints": 208,
        "totalEarnPoints": 1108,
        "totalRedeemPoints": 900,
        "totalSaleAmount": 36330.94
      },
      "benefit": {
        "mileage": 208,
        "max_mileage_percent": 50,
        "discount_percent": 5,
        "max_discount_price": 0,
        "birthday_discount_percent": 30,
        "max_birthday_price": 5000
      }
    },
    "mileage": {
      "current": 208,
      "available": 208,
      "use": 208
    },
    "couponInfo": {
      "no": "EE4EEDE03E762A2AA2",
      "couponType": "Discount",
      "discountName": "8折优惠",
      "eventId": "EE2017030024"
    },
    "info": {
      "receipt": "193018485875930103",
      "casher": "nancy"
    },
    "payments": [
      {
        "method": "alipay",
        "amount": 690
      }
    ],
    "userId": 1000002,
    "spotId": 2000001,
    "createdAt": "2017-04-13T15:50:41Z",
    "updatedAt": "2017-04-13T16:00:48.401563037Z",
    "items": [
      {
        "sku": {
          "id": 184184,
          "contentId": 15579,
          "name": "EERA72505B, (30)Yellow, (160)160",
          "code": "EERA72505B30160",
          "listPrice": 498,
          "salePrice": 398,
          "discountName": "8折优惠",
          "brandCode": "EE",
          "contentCode": "EE",
          "images": {
              "large": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL.jpg",
                  "width": 385,
                  "height": 500
              },
              "medium": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL160_.jpg",
                  "width": 123,
                  "height": 160
              },
              "small": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL75_.jpg",
                  "width": 58,
                  "height": 75
              }
          },
          "options": [
            {
              "k": "Size",
              "v": "(160)160"
            },
            {
              "k": "Color",
              "v": "(30)Yellow"
            }
          ]
        },
        "quantity": 1,
        "listPrice": 498,
        "salePrice": 398,
        "discount": 100
      },
      {
        "sku": {
          "id": 184413,
          "contentId": 15621,
          "name": "EETA72553N, (59)Navy, (155)155",
          "code": "EETA72553N59155",
          "listPrice": 598,
          "salePrice": 500,
          "discountName": "EETA72553N Discount! ￥500",
          "brandCode": "EE",
          "contentCode": "EE",
          "images": {
              "large": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL.jpg",
                  "width": 385,
                  "height": 500
              },
              "medium": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL160_.jpg",
                  "width": 123,
                  "height": 160
              },
              "small": {
                  "url": "https://images-na.ssl-images-amazon.com/images/I/310neZo0MKL._SL75_.jpg",
                  "width": 58,
                  "height": 75
              }
          },
          "options": [
            {
              "k": "Size",
              "v": "(155)155"
            },
            {
              "k": "Color",
              "v": "(59)Navy"
            }
          ]
        },
        "quantity": 1,
        "listPrice": 598,
        "salePrice": 500,
        "discount": 98
      }
    ],
    "suggests": [
      {
        "name": "EERA72505 Bundle Sale",
        "desc": "",
        "listPrice": 796,
        "salePrice": 600,
        "startAt": "2017-04-13T11:32:47Z",
        "endAt": "2017-05-13T11:32:47Z",
        "channelId": 0,
        "virtualContents": [
          {
            "contentId": 15579,
            "listPrice": 498,
            "salePrice": 400
          },
          {
            "contentId": 15628,
            "listPrice": 298,
            "salePrice": 200
          }
        ]
      }
    ]
  },
  "success": true,
  "error": {}
}
```