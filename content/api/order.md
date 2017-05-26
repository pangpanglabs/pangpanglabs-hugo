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
|cartId|Yes|string|
|uid|No|string|

#### Example

`pp://staging/order/place-order?cartId=1&uid=20170501138400031`

Success:
```
{
    "result": {
        "id": "1212",
        "orderNo": "14945206951212",
        "uid": "20170501138400031",
        "quantity": 4,
        "listPrice": 3588,
        "salePrice": 2511.6,
        "discount": 1076.4,
        "items": [
            {
                "seq": 1,
                "skuId": 184184,
                "sku": {
                    "id": 184184,
                    "contentId": 21673,
                    "name": "EEYC64T51M, (62)Hunter, (160)160",
                    "code": "EEYC64T51M62160",
                    "images": null,
                    "options": [
                        {
                            "k": "Size",
                            "v": "(160)160"
                        },
                        {
                            "k": "Color",
                            "v": "(62)Hunter"
                        }
                    ],
                    "brandCode": "EE",
                    "contentCode": "EEYC64T51M",
                    "listPrice": 598,
                    "offers": [
                        {
                            "id": 1952,
                            "name": "百货店vip 9折",
                            "salePrice": 538.2,
                            "channelName": "北京汉光",
                            "startAt": "2017-05-01T00:00:00Z",
                            "endAt": "2017-06-02T00:00:00Z",
                            "requirement": {
                                    "customerGroup": "VIP"
                            }
                        }
                    ]
                },
                "offer": {
                    "id": 1952,                    
                    "name": "百货店vip 9折",
                    "salePrice": 538.2,
                    "channelName": "北京汉光",
                    "startAt": "2017-05-01T00:00:00Z",
                    "endAt": "2017-06-02T00:00:00Z",
                    "requirement": {
                                    "customerGroup": "VIP"
                            }
                },
                "quantity": 2,
                "listPrice": 1196,
                "salePrice": 1076.4,
                "discount": 119.6
            },
            {
                "seq": 2,
                "skuId": 184184,
                "sku": {
                    "id": 184184,
                    "contentId": 21673,
                    "name": "EEYC64T51M, (62)Hunter, (160)160",
                    "code": "EEYC64T51M62160",
                    "images": null,
                    "options": [
                        {
                            "k": "Size",
                            "v": "(160)160"
                        },
                        {
                            "k": "Color",
                            "v": "(62)Hunter"
                        }
                    ],
                    "brandCode": "EE",
                    "contentCode": "EEYC64T51M",
                    "listPrice": 598,
                    "offers": [
                        {
                            "id": 1952,
                            "code": "C108097",
                            "name": "百货店vip 9折",
                            "salePrice": 538.2,
                            "channelId": 12,
                            "channelName": "北京汉光",
                            "startAt": "2017-05-01T00:00:00Z",
                            "endAt": "2017-06-02T00:00:00Z",
                            "requirement": {}
                        }
                    ]
                },
                "offer": null,
                "quantity": 2,
                "listPrice": 1196,
                "salePrice": 717.6,
                "discount": 478.4
            },
            {
                "seq": 3,
                "skuId": 186184,
                "sku": {
                    "id": 186184,
                    "contentId": 24108,
                    "name": "EETJ72403A, (52)D/Blue, (165)165",
                    "code": "EETJ72403A52165",
                    "images": null,
                    "options": [
                        {
                            "k": "Size",
                            "v": "(165)165"
                        },
                        {
                            "k": "Color",
                            "v": "(52)D/Blue"
                        }
                    ],
                    "brandCode": "EE",
                    "contentCode": "EETJ72403A",
                    "listPrice": 598,
                    "offers": [
                        {
                            "id": 1952,
                            "code": "C108097",
                            "name": "百货店vip 9折",
                            "salePrice": 538.2,
                            "channelId": 12,
                            "channelName": "北京汉光",
                            "startAt": "2017-05-01T00:00:00Z",
                            "endAt": "2017-06-02T00:00:00Z",
                            "requirement": {}
                        }
                    ]
                },
                "offer": null,
                "quantity": 2,
                "listPrice": 1196,
                "salePrice": 717.6,
                "discount": 478.4
            }
        ],
        "customerId": 1065586,
        "couponInfo": {
            "no": "EEB5AA500E8539665E",
            "title": "多级折扣型",
            "desc": "多级折扣型",
            "startAt": "2017-05-02T16:00:00Z",
            "endAt": "2017-06-01T15:59:59Z",
            "enable": true,
            "couponType": "Discount",
            "eventId": "EE2017050013",
            "offerName": "多级折扣型"
        },
        "customerInfo": {
            "id": 1065586,
            "no": "0000053147",
            "brandCode": "EE",
            "mobile": "13818448893",
            "grade": 3,
            "cardType": "diamondCard",
            "mileage": {
                "currentPoints": 78,
                "totalEarnPoints": 1227,
                "totalRedeemPoints": 1149,
                "totalSaleAmount": 39422.94
            },
            "benefit": {
                "mileage": 78,
                "max_mileage_percent": 50,
                "discount_percent": 5,
                "max_discount_price": 0,
                "birthday_discount_percent": 0,
                "max_birthday_price": 0
            }
        },
        "mileage": {
            "current": 78,
            "available": 78,
            "use": 78
        },
        "info": {
            "cashierName": "6000026999",
            "chiefBrandCode": "EE",
            "shopCode": "C30R",
            "shopInfo": [
                {
                    "brandCode": "EE",
                    "isChief": true,
                    "shopCode": "C30R"
                }
            ]
        },
        "payments": [
            {
                "method": "ALIPAY",
                "amount": 50
            },
            {
                "method": "WXPAY",
                "amount": 350
            },
            {
                "method": "CASH",
                "amount": 1000
            }
        ],
        "userId": 14,        
        "spotId": 26,
        "tenantId": 4,
        "createdAt": "2017-05-11T16:38:15.499788223Z"
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
|orderId|-|string|
|orderNo|-|string|
|uid|-|string|

**One of `orderId`, `orderNo` or `uid` is a required.**

#### Example

`pp://staging/order/get-order?orderId=132`


---

## All orders

`/order/all-orders`

#### Parameters


|Name|Required|Type|
|---|---|---|
|skipCount|No|number|
|maxResultCount|No|number|
|startAt|No|string|
|endAt|No|string|

#### Example

Request: 

`pp://staging/order/all-orders?skipCount=0&maxResultCount=10&startAt=2017-05-01&endAt=2017-05-31`

Success:
```
{
    "result": {
        "items": [
            /* ... */         
        ],
        "totalCount": 28
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
|parentOrderId|-|string|
|parentOrderNo|-|string|
|parentUid|-|string|
|uid|No|string|

**One of `parentOrderId`, `parentOrderNo` or `parentUid` is a required.**

#### Example

`pp://staging/order/return?parentOrderId=132&uid=1705021039402`

## Return order and resale

`/order/return-and-resale`

#### Parameters


|Name|Required|Type|
|---|---|---|
|parentOrderId|-|string|
|parentOrderNo|-|string|
|parentUid|-|string|
|uid|No|string|
|items[`seq`]|Yes|integer|

**One of `parentOrderId`, `parentOrderNo` or `parentUid` is a required.**

#### Example

Request: 

`pp://staging/order/return-and-resale?parentOrderId=132&uid=1705021039402&items[2]=2&items[1]=1`

Success:
```
{
    "result": {
        "order": {
            /* returned order */
        },
        "cart": {
            /* resale cart */
        }
    },
    "success": true,
    "error": {}
}
```