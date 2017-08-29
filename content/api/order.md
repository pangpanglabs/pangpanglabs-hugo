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
    "id": "10685",
    "orderNo": "15028499890685",
    "uid": "EE20170815140238",
    "parentId": "0",
    "quantity": 6,
    "listPrice": 1638,
    "salePrice": 1373.2,
    "discount": 264.8,
    "items": [
        {
            "seq": 1,
            "sku": {
                "id": 108235,
                "name": "XXXXXS601D, (26)L/Pink, (FRE)FREE",
                "contentId": 15664,
                "brandId": 1,
                "code": "XXXXXS601D26FRE",
                "contentCode": "XXXXXS601D",
                "brandCode": "EE",
                "listPrice": 128,
                "options": [
                    { "k": "Size", "v": "(FRE)FREE" },
                    { "k": "Color", "v": "(26)L/Pink" }
                ],
                "attributes": [
                    { "k": "ItemCode", "v": "AB" },
                    { "k": "Year", "v": "2017" },
                    { "k": "SeasonCode", "v": "S" },
                    { "k": "SaleMonth", "v": "6" },
                    { "k": "ContentTypeCode", "v": "P" }
                ]
            },
            "quantity": 1,
            "listPrice": 128,
            "salePrice": 115.2,
            "discount": 12.8,
            "catalogOffer": {
                "id": 613,
                "name": "vip(9)",
                "code": "C000030",
                "discount": 12.8
            },
            "wcsOffer": null,
            "cartOffers": null,
            "unitSalePrice": 115.2,
            "status": "closed"
        },
        {
            "seq": 2,
            "sku": {
                "id": 108236,
                "name": "XXXXXS601D, (NA)合并颜色, (ONA)合并尺寸",
                "contentId": 15664,
                "brandId": 1,
                "code": "XXXXXS601DNAONA",
                "contentCode": "XXXXXS601D",
                "brandCode": "EE",
                "listPrice": 128,
                "options": [
                    { "k": "Size", "v": "(ONA)통합사이즈" },
                    { "k": "Color", "v": "(NA)통합칼라" }
                ],
                "attributes": [
                    { "k": "ItemCode", "v": "AB" },
                    { "k": "Year", "v": "2017" },
                    { "k": "SeasonCode", "v": "S" },
                    { "k": "SaleMonth", "v": "6" },
                    { "k": "ContentTypeCode", "v": "P" }
                ]
            },
            "quantity": 1,
            "listPrice": 128,
            "salePrice": 115.2,
            "discount": 12.8,
            "catalogOffer": {
                "id": 613,
                "name": "vip(9)",
                "code": "C000030",
                "discount": 12.8
            },
            "wcsOffer": null,
            "cartOffers": null,
            "unitSalePrice": 115.2,
            "status": "closed"
        },
        {
            "seq": 3,
            "sku": {
                "id": 94688,
                "name": "XXXXX401, XXX, XXX",
                "contentId": 471,
                "brandId": 1,
                "code": "XXXXX401XXXXXX",
                "contentCode": "XXXXX401",
                "brandCode": "EE",
                "listPrice": 378,
                "options": [
                    { "k": "Size", "v": "(XXX)N/A" },
                    { "k": "Color", "v": "(XXX)N/A" }
                ],
                "attributes": [
                    { "k": "ItemCode", "v": "AB" },
                    { "k": "Year", "v": "2007" },
                    { "k": "SeasonCode", "v": "2" },
                    { "k": "SaleMonth", "v": "4" },
                    { "k": "ContentTypeCode", "v": "P" }
                ]
            },
            "quantity": 2,
            "listPrice": 756,
            "salePrice": 604.8,
            "discount": 151.2,
            "catalogOffer": null,
            "wcsOffer": {
                "id": 0,
                "name": "POS3.0使用_8折券",
                "code": "EE2017050023",
                "couponNo": "EEXXXXXXXXXX",
                "discount": 151.2
            },
            "cartOffers": null,
            "unitSalePrice": 302.4,
            "status": "closed"
        },
        {
            "seq": 4,
            "sku": {
                "id": 94686,
                "name": "XXXXX401, 281, XXX",
                "contentId": 471,
                "brandId": 1,
                "code": "XXXXX401281XXX",
                "contentCode": "XXXXX401",
                "brandCode": "EE",
                "listPrice": 378,
                "options": [
                    { "k": "Size", "v": "(XXX)N/A" },
                    { "k": "Color", "v": "(281)brown" }
                ],
                "attributes": [
                    { "k": "ItemCode", "v": "AB" },
                    { "k": "Year", "v": "2007" },
                    { "k": "SeasonCode", "v": "2" },
                    { "k": "SaleMonth", "v": "4" },
                    { "k": "ContentTypeCode", "v": "P" }
                ]
            },
            "quantity": 1,
            "listPrice": 378,
            "salePrice": 302.4,
            "discount": 75.6,
            "catalogOffer": null,
            "wcsOffer": {
                "id": 0,
                "name": "POS3.0使用_8折券",
                "code": "EE2017050023",
                "discount": 75.6
            },
            "cartOffers": null,
            "unitSalePrice": 302.4,
            "status": "closed"
        },
        {
            "seq": 5,
            "sku": {
                "id": 1944,
                "name": "XXXXX102, 781, 000",
                "contentId": 463,
                "brandId": 1,
                "code": "XXXXX102781000",
                "contentCode": "XXXXX102",
                "brandCode": "EE",
                "listPrice": 248,
                "options": [
                    { "k": "Size", "v": "(000)生产代表尺寸" },
                    { "k": "Color", "v": "(781)navy" }
                ],
                "attributes": [
                    { "k": "ItemCode", "v": "AB" },
                    { "k": "Year", "v": "2007" },
                    { "k": "SeasonCode", "v": "1" },
                    { "k": "SaleMonth", "v": "1" },
                    { "k": "ContentTypeCode", "v": "P" }
                ]
            },
            "quantity": 1,
            "listPrice": 248,
            "salePrice": 235.6,
            "discount": 12.4,
            "catalogOffer": {
                "id": 612,
                "name": "vip(9.5)",
                "code": "C000029",
                "discount": 12.4
            },
            "wcsOffer": null,
            "cartOffers": null,
            "unitSalePrice": 235.6,
            "status": "closed"
        }
    ],
    "customerId": 1065576,
    "couponNo": "EEXXXXXXXXXX",
    "couponInfo": {
        "no": "EEXXXXXXXXXX",
        "title": "POS3.0使用_8折券",
        "desc": "POS3.0使用_8折券",
        "startAt": "2017-05-14T16:00:00Z",
        "endAt": "2017-09-30T15:59:59Z",
        "enable": true,
        "couponType": "Discount",
        "eventId": "EEXXXXXXXX",
        "offerName": "POS3.0使用_8折券"
    },
    "customerInfo": {
        "id": 1065576,
        "no": "0000211453",
        "brandCode": "EE",
        "mobile": "13900001234",
        "grade": 1,
        "cardType": "diamondCard",
        "mileage": {
            "currentPoints": 879,
            "totalEarnPoints": 9497,
            "totalRedeemPoints": 8684,
            "totalSaleAmount": 211563.77
        },
        "benefit": {
            "can_redeem_mileage": true,
            "min_redeem_points": 100,
            "mileage": 879,
            "max_mileage_percent": 50,
            "discount_percent": 0,
            "birthday_discount_percent": 0,
            "max_birthday_price": 0
        },
        "profile": {
            "name": "名字",
            "gender": "F",
            "birthday": "1986-09-29",
            "email": "email@p2shop.cn",
            "married": false,
            "address": "北京XXXXXXXX",
            "addressDetail": "XXXXXXXX"
        }
    },
    "mileage": {
        "current": 879,
        "available": 686,
        "use": 100
    },
    "info": null,
    "payments": [
        { "seq": 1, "method": "alipay", "amount": 1000 },
        { "seq": 2, "method": "wxpay", "amount": 200 },
        { "seq": 3, "method": "creditcard", "amount": 50 },
        { "seq": 4, "method": "cash", "amount": 23.2 }
    ],
    "catalogOffers": [
        {
            "id": 613,
            "name": "vip(9)",
            "code": "C000030",
            "discount": 153.6
        },
        {
            "id": 612,
            "name": "vip(9.5)",
            "code": "C000029",
            "discount": 74.4
        }
    ],
    "cartOffers": null,
    "wcsOffer": {
        "name": "POS3.0使用_8折券",
        "code": "EE2017050023",
        "couponNo": "EEXXXXXXXXXX",
        "discount": 226.8
    },
    "userId": 171,
    "salesmanId": 174,
    "deviceId": "",
    "spotId": 12,
    "tenantId": 2,
    "channelId": 413,
    "createdAt": "2017-08-16T02:19:49.328005471Z",
    "status": "created",
    "spot": {
        "code": "EE-C30X",
        "name": "EE 杭州银泰",
        "shopInfo": [
            {
                "brandCode": "EE",
                "isChief": false,
                "shopCode": "C30X"
            }
        ]
    }
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

## Edit Payment

`/order/edit-payment`

####  Parameters


|Name|Required|Type|Desc|
|---|---|---|---|
|orderId|Yes|string|
|seq|Yes|integer|payment seq|
|transNo|No|string|-|
|returnTransNo|No|string|-|
|referenceNo|No|string|-|
|terminalId|No|string|-|
|creditCardNo|No|string|-|
|creditCardCode|No|string|-|
|couponNo|No|string|-|
|couponType|No|string|-|

#### Example

`pp://staging//order/edit-payment?orderId=132&seq=1&transNo=xxxxxxxx&terminalId=xxxxxxxx`

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