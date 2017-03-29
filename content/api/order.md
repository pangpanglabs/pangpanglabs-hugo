+++
title = "Order"
weight = 5
toc = true
+++


## Place order

`/order/place-order`

#### Parameters


|Name|Required|Type|
|---|---|---|
|cartId|Yes|number|

#### Example

Request: 

`pp://staging/order/place-order?cartId=1`

Success:
```
{
    "result": {
        "id": 132,
        "orderNo": "14907758150132",
        "quantity": 3,
        "listPrice": 125.5,
        "salePrice": 114.3,
        "discount": 11.2,
        "items": [
            {
                "seq": 1,
                "skuId": 169,
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
                "seq": 2,
                "skuId": 2454,
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
        "couponNo": "EE4E52FEF46F7B30DE",
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
        "info": {
            "casher": "nancy",
            "receipt": "193018485875930103"
        },
        "discountInfo": {
            "couponType": "Discount",
            "discountName": "8折优惠",
            "eventId": "EE2017030024"
        },
        "payments": null,
        "userId": 1000001,
        "deviceId": "",
        "spotId": 2000001,
        "tenantId": 10,
        "createdAt": "2017-03-29T08:23:35.27528848Z"
    },
    "success": true,
    "error": {}
}
```

---

## All orders

`/order/all-orders`

#### Parameters


|Name|Required|Type|
|---|---|---|
|skipCount|No|number|
|maxResultCount|No|number|

#### Example

Request: 

`pp://staging/order/all-orders?skipCount=0&maxResultCount=10`

Success:
```
{
    "result": {
        "items": [
            {
                "id": 132,
                "orderNo": "14907758150132",
                "quantity": 3,
                "listPrice": 125.5,
                "salePrice": 114.3,
                "discount": 11.2,
                "items": null,
                "customerId": 0,
                "couponNo": "EE4E52FEF46F7B30DE",
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
                "info": {
                    "casher": "nancy",
                    "receipt": "193018485875930103"
                },
                "discountInfo": {
                    "couponType": "Discount",
                    "discountName": "8折优惠",
                    "eventId": "EE2017030024"
                },
                "payments": null,
                "userId": 1000001,
                "deviceId": "",
                "spotId": 2000001,
                "tenantId": 10,
                "createdAt": "2017-03-29T08:23:35Z"
            },
            {
                "id": 133,
                "parentId": 132,
                "orderNo": "14907759790133",
                "quantity": -3,
                "listPrice": -125.5,
                "salePrice": -114.3,
                "discount": -11.2,
                "items": null,
                "customerId": 0,
                "couponNo": "EE4E52FEF46F7B30DE",
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
                "info": {
                    "casher": "nancy",
                    "receipt": "193018485875930103"
                },
                "discountInfo": {
                    "couponType": "Discount",
                    "discountName": "8折优惠",
                    "eventId": "EE2017030024"
                },
                "payments": null,
                "userId": 1000001,
                "deviceId": "",
                "spotId": 2000001,
                "tenantId": 10,
                "createdAt": "2017-03-29T08:26:19Z"
            }
        ],
        "totalCount": 2
    },
    "success": true,
    "error": {}
}
```

## Return order

`/order/return`

#### Parameters


|Name|Required|Type|
|---|---|---|
|orderId|Yes|number|

#### Example

Request: 

`pp://staging/order/return?orderId=132`

Success:
```
{
    "result": {
        "id": 133,
        "parentId": 132,
        "orderNo": "14907759790133",
        "quantity": -3,
        "listPrice": -125.5,
        "salePrice": -114.3,
        "discount": -11.2,
        "items": [
            {
                "seq": 0,
                "skuId": 169,
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
                "quantity": -1,
                "listPrice": -69.5,
                "salePrice": -69.5,
                "discount": 0
            },
            {
                "seq": 0,
                "skuId": 2454,
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
                "quantity": -2,
                "listPrice": -56,
                "salePrice": -44.8,
                "discount": -11.2
            }
        ],
        "couponNo": "EE4E52FEF46F7B30DE",
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
        "info": {
            "casher": "nancy",
            "receipt": "193018485875930103"
        },
        "discountInfo": {
            "couponType": "Discount",
            "discountName": "8折优惠",
            "eventId": "EE2017030024"
        },
        "payments": null,
        "userId": 1000001,
        "deviceId": "",
        "spotId": 2000001,
        "tenantId": 10,
        "createdAt": "2017-03-29T08:26:19.668202277Z"
    },
    "success": true,
    "error": {}
}
```