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
    "id": 326,
    "tenantId": 10,
    "items": null,
    "listPrice": 0,
    "salePrice": 0,
    "quantity": 0,
    "discount": 0,
    "remainAmount": 0,
    "customerInfo": null,
    "couponNo": "",
    "info": null,
    "discountInfo": null,
    "payments": null,
    "userId": 1000001,
    "spotId": 2000001,
    "createdAt": "2017-03-29T07:47:02.773134948Z",
    "updatedAt": "0001-01-01T00:00:00Z"
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

`pp://staging/cart/add-item?cartId=326&skuId=169&quantity=2`

Success:
```
{
  "result": {
    "id": 326,
    "tenantId": 10,
    "items": [
      {
        "sku": {
          "id": 169,
          "contentId": 10,
          "name": "Calvin Klein Jeans Women's Gmt Dyed Ankle Skinny Pant, Monument, 26",
          "code": "42AB600-1",
          "listPrice": 69.5,
          "salePrice": 69.5,
          "brandCode": "Calvin Klein",
          "contentCode": "42AB600",
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
              "v": "26"
            },
            {
              "k": "Color",
              "v": "Monument"
            }
          ]
        },
        "quantity": 2,
        "listPrice": 139,
        "salePrice": 139,
        "discount": 0
      }
    ],
    "listPrice": 139,
    "salePrice": 139,
    "quantity": 2,
    "discount": 0,
    "remainAmount": 139,
    "customerInfo": null,
    "couponNo": "",
    "info": null,
    "discountInfo": null,
    "payments": null,
    "userId": 1000001,
    "spotId": 2000001,
    "createdAt": "2017-03-29T07:47:02Z",
    "updatedAt": "2017-03-29T07:47:54.783140997Z"
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

`pp://staging/cart/remove-item?cartId=326&skuId=169&quantity=1`

Success:
```
{
  "result": {
    "id": 326,
    "tenantId": 10,
    "items": [
      {
        "sku": {
          "id": 169,
          "contentId": 10,
          "name": "Calvin Klein Jeans Women's Gmt Dyed Ankle Skinny Pant, Monument, 26",
          "code": "42AB600-1",
          "listPrice": 69.5,
          "salePrice": 69.5,
          "brandCode": "Calvin Klein",
          "contentCode": "42AB600",
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
              "v": "26"
            },
            {
              "k": "Color",
              "v": "Monument"
            }
          ]
        },
        "quantity": 1,
        "listPrice": 69.5,
        "salePrice": 69.5,
        "discount": 0
      }
    ],
    "listPrice": 69.5,
    "salePrice": 69.5,
    "quantity": 1,
    "discount": 0,
    "remainAmount": 69.5,
    "customerInfo": null,
    "couponNo": "",
    "info": null,
    "discountInfo": null,
    "payments": null,
    "userId": 1000001,
    "spotId": 2000001,
    "createdAt": "2017-03-29T07:47:02Z",
    "updatedAt": "2017-03-29T07:49:29.971205281Z"
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
        "id": 326,
        "tenantId": 10,
        "items": [
            {
                "sku": {
                    "id": 169,
                    "contentId": 10,
                    "name": "Calvin Klein Jeans Women's Gmt Dyed Ankle Skinny Pant, Monument, 26",
                    "code": "42AB600-1",
                    "listPrice": 69.5,
                    "salePrice": 69.5,
                    "brandCode": "Calvin Klein",
                    "contentCode": "42AB600",
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
                            "v": "26"
                        },
                        {
                            "k": "Color",
                            "v": "Monument"
                        }
                    ]
                },
                "quantity": 1,
                "listPrice": 69.5,
                "salePrice": 69.5,
                "discount": 0
            }
        ],
        "listPrice": 69.5,
        "salePrice": 69.5,
        "quantity": 1,
        "discount": 0,
        "remainAmount": 69.5,
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
        "discountInfo": null,
        "payments": null,
        "userId": 1000001,
        "spotId": 2000001,
        "createdAt": "2017-03-29T07:47:02Z",
        "updatedAt": "2017-03-29T07:49:29.971205281Z"
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
    "id": 326,
    "tenantId": 10,
    "items": [
      {
        "sku": {
          "id": 169,
          "contentId": 10,
          "name": "Calvin Klein Jeans Women's Gmt Dyed Ankle Skinny Pant, Monument, 26",
          "code": "42AB600-1",
          "listPrice": 69.5,
          "salePrice": 69.5,
          "brandCode": "Calvin Klein",
          "contentCode": "42AB600",
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
              "v": "26"
            },
            {
              "k": "Color",
              "v": "Monument"
            }
          ]
        },
        "quantity": 1,
        "listPrice": 69.5,
        "salePrice": 69.5,
        "discount": 0
      },
      {
        "sku": {
          "id": 2454,
          "contentId": 445,
          "name": "EEAA8A011, 101, 000",
          "code": "EEAA8A011101000",
          "listPrice": 28,
          "salePrice": 28,
          "brandCode": "EE",
          "contentCode": "EEAA8A011",
          "images": null,
          "options": [
            {
              "k": "Size",
              "v": "(000)生产代表尺寸"
            },
            {
              "k": "Color",
              "v": "(101)red"
            }
          ]
        },
        "quantity": 2,
        "listPrice": 56,
        "salePrice": 44.8,
        "discount": 11.2
      }
    ],
    "listPrice": 125.5,
    "salePrice": 114.3,
    "quantity": 3,
    "discount": 11.2,
    "remainAmount": 114.3,
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
    "couponNo": "EE4E52FEF46F7B30DE",    
    "discountInfo": {
      "couponType": "Discount",
      "discountName": "8折优惠",
      "eventId": "EE2017030024"
    },
    "info": {},
    "payments": null,
    "userId": 1000001,
    "spotId": 2000001,
    "createdAt": "2017-03-29T07:47:02Z",
    "updatedAt": "2017-03-29T08:12:44.017761577Z"
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

`pp://staging/cart/set-info?cartId=326&receipt=193018485875930103&casher=nancy`

Success:
```
{
  "result": {
    "id": 326,
    "tenantId": 10,
    "items": [
      {
        "sku": {
          "id": 169,
          "contentId": 10,
          "name": "Calvin Klein Jeans Women's Gmt Dyed Ankle Skinny Pant, Monument, 26",
          "code": "42AB600-1",
          "listPrice": 69.5,
          "salePrice": 69.5,
          "brandCode": "Calvin Klein",
          "contentCode": "42AB600",
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
              "v": "26"
            },
            {
              "k": "Color",
              "v": "Monument"
            }
          ]
        },
        "quantity": 1,
        "listPrice": 69.5,
        "salePrice": 69.5,
        "discount": 0
      },
      {
        "sku": {
          "id": 2454,
          "contentId": 445,
          "name": "EEAA8A011, 101, 000",
          "code": "EEAA8A011101000",
          "listPrice": 28,
          "salePrice": 28,
          "brandCode": "EE",
          "contentCode": "EEAA8A011",
          "images": null,
          "options": [
            {
              "k": "Size",
              "v": "(000)生产代表尺寸"
            },
            {
              "k": "Color",
              "v": "(101)red"
            }
          ]
        },
        "quantity": 2,
        "listPrice": 56,
        "salePrice": 44.8,
        "discount": 11.2
      }
    ],
    "listPrice": 125.5,
    "salePrice": 114.3,
    "quantity": 3,
    "discount": 11.2,
    "remainAmount": 114.3,
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
    "couponNo": "EE4E52FEF46F7B30DE",    
    "discountInfo": {
      "couponType": "Discount",
      "discountName": "8折优惠",
      "eventId": "EE2017030024"
    },
    "info": {
        "casher": "nancy",
        "receipt": "193018485875930103"
    },
    "payments": null,
    "userId": 1000001,
    "spotId": 2000001,
    "createdAt": "2017-03-29T07:47:02Z",
    "updatedAt": "2017-03-29T08:12:44.017761577Z"
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

`pp://staging/cart/remove-cart?cartId=326`

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
      "id": 326,
      "tenantId": 10,    
      "listPrice": 125.5,
      "salePrice": 114.3,
      "quantity": 3,
      "discount": 11.2,
      "remainAmount": 114.3,
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
      "couponNo": "EE4E52FEF46F7B30DE",    
      "discountInfo": {
        "couponType": "Discount",
        "discountName": "8折优惠",
        "eventId": "EE2017030024"
      },
      "info": {
          "casher": "nancy",
          "receipt": "193018485875930103"
      },
      "payments": null,
      "userId": 1000001,
      "spotId": 2000001,
      "createdAt": "2017-03-29T07:47:02Z",
      "updatedAt": "2017-03-29T08:12:44.017761577Z"
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

`pp://staging/cart/get-cart?cartId=326`

Success:
```
{
  "result": {
    "id": 326,
    "tenantId": 10,
    "items": [
      {
        "sku": {
          "id": 169,
          "contentId": 10,
          "name": "Calvin Klein Jeans Women's Gmt Dyed Ankle Skinny Pant, Monument, 26",
          "code": "42AB600-1",
          "listPrice": 69.5,
          "salePrice": 69.5,
          "brandCode": "Calvin Klein",
          "contentCode": "42AB600",
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
              "v": "26"
            },
            {
              "k": "Color",
              "v": "Monument"
            }
          ]
        },
        "quantity": 1,
        "listPrice": 69.5,
        "salePrice": 69.5,
        "discount": 0
      },
      {
        "sku": {
          "id": 2454,
          "contentId": 445,
          "name": "EEAA8A011, 101, 000",
          "code": "EEAA8A011101000",
          "listPrice": 28,
          "salePrice": 28,
          "brandCode": "EE",
          "contentCode": "EEAA8A011",
          "images": null,
          "options": [
            {
              "k": "Size",
              "v": "(000)生产代表尺寸"
            },
            {
              "k": "Color",
              "v": "(101)red"
            }
          ]
        },
        "quantity": 2,
        "listPrice": 56,
        "salePrice": 44.8,
        "discount": 11.2
      }
    ],
    "listPrice": 125.5,
    "salePrice": 114.3,
    "quantity": 3,
    "discount": 11.2,
    "remainAmount": 114.3,
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
    "couponNo": "EE4E52FEF46F7B30DE",    
    "discountInfo": {
      "couponType": "Discount",
      "discountName": "8折优惠",
      "eventId": "EE2017030024"
    },
    "info": {
        "casher": "nancy",
        "receipt": "193018485875930103"
    },
    "payments": null,
    "userId": 1000001,
    "spotId": 2000001,
    "createdAt": "2017-03-29T07:47:02Z",
    "updatedAt": "2017-03-29T08:12:44.017761577Z"
  },
  "success": true,
  "error": {}
}
```