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
                    "discountName": "",
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
                    "salePrice": 22.4,
                    "discountName": "8折优惠",
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
        "couponInfo": {
            "no": "EE4E52FEF46F7B30DE",
            "couponType": "Discount",            
            "discountName": "8折优惠",
            "eventId": "EE2017030024"
        }
        "customerInfo": {
            "id": 1065586,
            "no": "0000053147",
            "brandCode": "EE",
            "mobile": "13818448893",
            "grade": 3,
            "cardType": "purpleCard",
            "mileage": {
                "currentPoints": 9000,
                "totalEarnPoints": 10000,
                "totalRedeemPoints": 10,
                "totalSaleAmount": "345.0"
            }
        },
        "mileage": {        
            "use": 0
        },
        "info": {
            "casher": "nancy",
            "receipt": "193018485875930103"
        },        
        "payments": [
        {
            "method": "alipay",
            "amount": 114.3
        }
        "userId": 1000001,
        "spotId": 2000001,
        "tenantId": 12,
        "createdAt": "2017-03-29T08:23:35.27528848Z"
    },
    "success": true,
    "error": {}
}
```

---

## Get order

`/order/get-order`

#### Parameters


|Name|Required|Type|
|---|---|---|
|orderId|Yes|number|

#### Example

Request: 

`pp://staging/order/get-order?orderId=132`

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
                    "discountName": "",
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
                    "salePrice": 22.4,
                    "discountName": "8折优惠",
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
        "couponInfo": {
            "no": "EE4E52FEF46F7B30DE",
            "couponType": "Discount",            
            "discountName": "8折优惠",
            "eventId": "EE2017030024"
        }
        "customerInfo": {
            "id": 1065586,
            "no": "0000053147",
            "brandCode": "EE",
            "mobile": "13818448893",
            "grade": 3,
            "cardType": "purpleCard",
            "mileage": {
                "currentPoints": 9000,
                "totalEarnPoints": 10000,
                "totalRedeemPoints": 10,
                "totalSaleAmount": "345.0"
            }
        },
        "mileage": {        
            "use": 0
        },
        "info": {
            "casher": "nancy",
            "receipt": "193018485875930103"
        },        
        "payments": [
        {
            "method": "alipay",
            "amount": 114.3
        }
        "userId": 1000001,
        "spotId": 2000001,
        "tenantId": 12,
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
                "couponInfo": {
                    "no": "EE4E52FEF46F7B30DE",
                    "couponType": "Discount",            
                    "discountName": "8折优惠",
                    "eventId": "EE2017030024"
                }
                "customerInfo": {
                    "id": 1065586,
                    "no": "0000053147",
                    "brandCode": "EE",
                    "mobile": "13818448893",
                    "grade": 3,
                    "cardType": "purpleCard",
                    "mileage": {
                        "currentPoints": 9000,
                        "totalEarnPoints": 10000,
                        "totalRedeemPoints": 10,
                        "totalSaleAmount": "345.0"
                    }
                },
                "mileage": {        
                    "use": 0
                },
                "info": {
                    "casher": "nancy",
                    "receipt": "193018485875930103"
                },        
                "payments": [
                {
                    "method": "alipay",
                    "amount": 114.3
                }
                "userId": 1000001,
                "spotId": 2000001,
                "tenantId": 12,
                "createdAt": "2017-03-29T08:23:35Z"
            }            
        ],
        "totalCount": 1
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
        "id": 132,
        "orderNo": "14907758150132",
        "quantity": -3,
        "listPrice": -125.5,
        "salePrice": -114.3,
        "discount": -11.2,
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
                    "discountName": "",
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
                "seq": 2,
                "skuId": 2454,
                "sku": {
                    "id": 2454,
                    "contentId": 445,
                    "name": "EEAA8A011, 101, 000",
                    "code": "EEAA8A011101000",
                    "listPrice": 28,
                    "salePrice": 22.4,
                    "discountName": "8折优惠",
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
        "couponInfo": {
            "no": "EE4E52FEF46F7B30DE",
            "couponType": "Discount",            
            "discountName": "8折优惠",
            "eventId": "EE2017030024"
        }
        "customerInfo": {
            "id": 1065586,
            "no": "0000053147",
            "brandCode": "EE",
            "mobile": "13818448893",
            "grade": 3,
            "cardType": "purpleCard",
            "mileage": {
                "currentPoints": 9000,
                "totalEarnPoints": 10000,
                "totalRedeemPoints": 10,
                "totalSaleAmount": "345.0"
            }
        },
        "mileage": {        
            "use": 0
        },
        "info": {
            "casher": "nancy",
            "receipt": "193018485875930103"
        },        
        "payments": [
        {
            "method": "alipay",
            "amount": -114.3
        }
        "userId": 1000001,
        "spotId": 2000001,
        "tenantId": 12,
        "createdAt": "2017-03-29T08:23:35.27528848Z"
    },
    "success": true,
    "error": {}
}
```