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
    "id": "83",
    "orderNo": "15005616990083",
    "uid": "",
    "quantity": 4,
    "listPrice": 1592,
    "salePrice": 1194,
    "discount": 398,
    "items": [
        {
            "seq": 1,
            "sku": {
                "id": 190264,
                "name": "EAAK68C01N, (16)L/Grey, FREE",
                "contentId": 23937,
                "brandId": 3,
                "code": "EAAK68C01N16FRE",
                "contentCode": "EAAK68C01N",
                "brandCode": "EA",
                "listPrice": 398,
                "options": [
                    { "k": "Size", "v": "FREE" },
                    { "k": "Color", "v": "(16)L/Grey" }
                ],
                "attributes": [
                    { "k": "ItemCode", "v": "AK" },
                    { "k": "Year", "v": "2016" },
                    { "k": "SeasonCode", "v": "8" },
                    { "k": "SaleMonth", "v": "C" },
                    { "k": "ContentTypeCode", "v": "P" }
                ],
                "offers": [
                    {
                        "id": 11808,
                        "code": "S2085822",
                        "name": "16年2件折0.8",
                        "salePrice": 159.2,
                        "channelId": 1218,
                        "channelName": "杭州奥特莱斯下沙店",
                        "startAt": "2017-04-24T00:00:00Z",
                        "endAt": "2017-07-31T00:00:00Z",
                        "fitAllContents": false,
                        "requirement": {}
                    },
                    {
                        "id": 11842,
                        "code": "S2142926",
                        "name": "16年5折",
                        "salePrice": 199,
                        "channelId": 1218,
                        "channelName": "杭州奥特莱斯下沙店",
                        "startAt": "2017-06-02T00:00:00Z",
                        "endAt": "2017-10-31T00:00:00Z",
                        "fitAllContents": false,
                        "requirement": {}
                    }
                ]
            },
            "offer": null,
            "quantity": 2,
            "listPrice": 796,
            "salePrice": 796,
            "discount": 0,
            "catalogOffer": null,
            "cartOffers": null,
            "unitSalePrice": 398,
            "status": "closed"
        },
        {
            "seq": 2,
            "sku": {
                "id": 190264,
                "name": "EAAK68C01N, (16)L/Grey, FREE",
                "contentId": 23937,
                "brandId": 3,
                "code": "EAAK68C01N16FRE",
                "contentCode": "EAAK68C01N",
                "brandCode": "EA",
                "listPrice": 398,
                "options": [
                    { "k": "Size", "v": "FREE" },
                    { "k": "Color", "v": "(16)L/Grey" }
                ],
                "attributes": [
                    { "k": "ItemCode", "v": "AK" },
                    { "k": "Year", "v": "2016" },
                    { "k": "SeasonCode", "v": "8" },
                    { "k": "SaleMonth", "v": "C" },
                    { "k": "ContentTypeCode", "v": "P" }
                ],
                "offers": [
                    {
                        "id": 11808,
                        "code": "S2085822",
                        "name": "16年2件折0.8",
                        "salePrice": 159.2,
                        "channelId": 1218,
                        "channelName": "杭州奥特莱斯下沙店",
                        "startAt": "2017-04-24T00:00:00Z",
                        "endAt": "2017-07-31T00:00:00Z",
                        "fitAllContents": false,
                        "requirement": {}
                    },
                    {
                        "id": 11842,
                        "code": "S2142926",
                        "name": "16年5折",
                        "salePrice": 199,
                        "channelId": 1218,
                        "channelName": "杭州奥特莱斯下沙店",
                        "startAt": "2017-06-02T00:00:00Z",
                        "endAt": "2017-10-31T00:00:00Z",
                        "fitAllContents": false,
                        "requirement": {}
                    }
                ]
            },
            "quantity": 2,
            "listPrice": 796,
            "salePrice": 398,
            "discount": 398,
            "catalogOffer": {
                "id": 11842,
                "name": "16年5折",
                "code": "S2142926"
            },
            "cartOffers": null,
            "unitSalePrice": 199,
            "status": "closed"
        }
    ],
    "customerId": 1065586,
    "couponNo": "",
    "couponInfo": {
        "no": "",
        "title": "",
        "desc": "",
        "startAt": "0001-01-01T00:00:00Z",
        "endAt": "0001-01-01T00:00:00Z",
        "enable": false,
        "couponType": "",
        "eventId": "",
        "offerName": ""
    },
    "customerInfo": {
        "id": 1065586,
        "no": "0000053147",
        "brandCode": "EE",
        "mobile": "13818448893",
        "grade": 2,
        "cardType": "diamondCard",
        "mileage": {
            "currentPoints": 761,
            "totalEarnPoints": 1988,
            "totalRedeemPoints": 1227,
            "totalSaleAmount": 55622.54
        },
        "benefit": {
            "can_redeem_mileage": true,
            "min_redeem_points": 100,
            "mileage": 761,
            "max_mileage_percent": 50,
            "discount_percent": 0,
            "birthday_discount_percent": 0,
            "max_birthday_price": 0
        },
        "profile": {
            "name": "李萍",
            "gender": "F",
            "birthday": "1974-04-11",
            "email": "",
            "married": true,
            "address": "青浦城东新村44号504",
            "addressDetail": ""
        }
    },
    "mileage": {
        "current": 761,
        "available": 597,
        "use": 0
    },
    "info": {
        "receipt": "29474594502101"
    },
    "payments": [
        { "method": "CREDITCARD", "amount": 50 },
        { "method": "WXPAY", "amount": 50 }
    ],
    "catalogOffers": [
        {
            "id": 11842,
            "name": "16年5折",
            "code": "S2142926"
        }
    ],
    "cartOffers": null,
    "userId": 55,
    "salesmanId": 55,
    "deviceId": "",
    "spotId": 13,
    "tenantId": 2,
    "channelId": 1218,
    "createdAt": "2017-07-20T14:41:39.371326956Z",
    "updatedAt": "2017-07-20T14:41:39.375963521Z",
    "status": "created" // "created", "canceled", "returned"
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