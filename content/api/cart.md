+++
title = "Cart"
weight = 4
toc = true
+++

## Cart result example

```
{
    "result": {
        "id": "219",
        "tenantId": 2,
        "channelId": 1218,
        "userId": 55,
        "salesmanId": 55,
        "spotId": 13,
        "listPrice": 1592,
        "salePrice": 1194,
        "quantity": 4,
        "discount": 398,
        "remainAmount": 1094,
        "cartOffers": null,
        "catalogOffers": [
            {
                "id": 11842,
                "name": "16年5折"
            }
        ],
        "customerInfo": {
            "benefit": {
                "birthday_discount_percent": 0,
                "can_redeem_mileage": true,
                "discount_percent": 0,
                "max_birthday_price": 0,
                "max_mileage_percent": 50,
                "mileage": 761,
                "min_redeem_points": 100
            },
            "brandCode": "EE",
            "cardType": "diamondCard",
            "grade": 2,
            "id": 1065586,
            "mileage": {
                "currentPoints": 761,
                "totalEarnPoints": 1988,
                "totalRedeemPoints": 1227,
                "totalSaleAmount": 55622.54
            },
            "mobile": "13818448893",
            "no": "0000053147",
            "profile": {
                "address": "青浦城东新村44号504",
                "addressDetail": "",
                "birthday": "1974-04-11",
                "email": "",
                "gender": "F",
                "married": true,
                "name": "李萍"
            }
        },
        "mileage": {
            "available": 597,
            "current": 761,
            "use": 0
        },
        "couponInfo": {
            "no": "EEB5AA500E8539665E",
            "title": "多级折扣型",
            "desc": "多级折扣型",
            "startAt": "2017-05-02T16:00:00Z",
            "enable": true,
            "couponType": "Discount",
            "eventId": "EE2017050013",
            "offerName": "多级折扣型",
            "endAt": "2017-06-01T15:59:59Z"
        },
        "info": {
            "receipt": "29474594502101"
        },
        "payments": [
            {
                "amount": 50,
                "method": "CREDITCARD"
            },
            {
                "amount": 50,
                "method": "WXPAY"
            }
        ],
        "items": [
            {
                "id": "247",
                "unitSalePrice": 199,
                "quantity": 2,
                "salePrice": 398,
                "listPrice": 796,
                "discount": 398,
                "cartOffers": null,
                "catalogOffer": {
                    "id": 11842,
                    "name": "16年5折"
                },
                "offer": {                             // DEPRECATED
                    "channelId": 1218,                 // DEPRECATED
                    "channelName": "杭州奥特莱斯下沙店",    // DEPRECATED
                    "code": "S2142926",                // DEPRECATED
                    "id": 11842,                       // DEPRECATED
                    "name": "16年5折",                  // DEPRECATED
                    "requirement": {},                 // DEPRECATED
                    "salePrice": 199,                  // DEPRECATED
                    "startAt": "2017-06-02T00:00:00Z", // DEPRECATED
                    "endAt": "2017-10-31T00:00:00Z"    // DEPRECATED
                },
                "sku": {
                    "attributes": [
                        {
                            "k": "ItemCode",
                            "v": "AK"
                        },
                        {
                            "k": "Year",
                            "v": "2016"
                        },
                        {
                            "k": "SeasonCode",
                            "v": "8"
                        },
                        {
                            "k": "SaleMonth",
                            "v": "C"
                        },
                        {
                            "k": "ContentTypeCode",
                            "v": "P"
                        }
                    ],
                    "brandCode": "EA",
                    "brandId": 3,
                    "code": "EAAK68C01N16FRE",
                    "contentCode": "EAAK68C01N",
                    "contentId": 23937,
                    "id": 190264,
                    "listPrice": 398,
                    "name": "EAAK68C01N, (16)L/Grey, FREE",
                    "offers": [
                        {
                            "id": 11808,
                            "channelId": 1218,
                            "channelName": "杭州奥特莱斯下沙店",
                            "code": "S2085822",
                            "name": "16年2件折0.8",
                            "requirement": {},
                            "salePrice": 159.2,
                            "startAt": "2017-04-24T00:00:00Z",
                            "endAt": "2017-07-31T00:00:00Z"
                        },
                        {
                            "id": 11822,
                            "channelId": 1218,
                            "channelName": "杭州奥特莱斯下沙店",
                            "code": "S2126643",
                            "name": "16年3件折8",
                            "requirement": {},
                            "salePrice": 159.2,
                            "startAt": "2017-05-22T00:00:00Z",
                            "endAt": "2017-10-31T00:00:00Z"
                        },
                        {
                            "id": 11842,
                            "channelId": 1218,
                            "channelName": "杭州奥特莱斯下沙店",
                            "code": "S2142926",
                            "name": "16年5折",
                            "requirement": {},
                            "salePrice": 199,
                            "startAt": "2017-06-02T00:00:00Z",
                            "endAt": "2017-10-31T00:00:00Z"
                        }
                    ],
                    "options": [
                        {
                            "k": "Size",
                            "v": "FREE"
                        },
                        {
                            "k": "Color",
                            "v": "(16)L/Grey"
                        }
                    ]
                }
            },
            {
                "id": "248",
                "unitSalePrice": 398,
                "quantity": 2,
                "salePrice": 796,
                "listPrice": 796,
                "discount": 0,
                "cartOffers": null,
                "catalogOffer": null,
                "offer": null,               // DEPRECATED
                "sku": {
                    "id": 190264,
                    "contentId": 23937,
                    "brandId": 3,
                    "name": "EAAK68C01N, (16)L/Grey, FREE",
                    "code": "EAAK68C01N16FRE",
                    "contentCode": "EAAK68C01N",
                    "brandCode": "EA",
                    "attributes": [
                        {
                            "k": "ItemCode",
                            "v": "AK"
                        },
                        {
                            "k": "Year",
                            "v": "2016"
                        },
                        {
                            "k": "SeasonCode",
                            "v": "8"
                        },
                        {
                            "k": "SaleMonth",
                            "v": "C"
                        },
                        {
                            "k": "ContentTypeCode",
                            "v": "P"
                        }
                    ],
                    "listPrice": 398,
                    "offers": [
                        {
                            "id": 11808,
                            "channelId": 1218,
                            "channelName": "杭州奥特莱斯下沙店",
                            "code": "S2085822",
                            "name": "16年2件折0.8",
                            "requirement": {},
                            "salePrice": 159.2,
                            "startAt": "2017-04-24T00:00:00Z",
                            "endAt": "2017-07-31T00:00:00Z"
                        },
                        {
                            "id": 11822,
                            "channelId": 1218,
                            "channelName": "杭州奥特莱斯下沙店",
                            "code": "S2126643",
                            "name": "16年3件折8",
                            "requirement": {},
                            "salePrice": 159.2,
                            "startAt": "2017-05-22T00:00:00Z",
                            "endAt": "2017-10-31T00:00:00Z"
                        },
                        {
                            "id": 11842,
                            "channelId": 1218,
                            "channelName": "杭州奥特莱斯下沙店",
                            "code": "S2142926",
                            "name": "16年5折",
                            "requirement": {},
                            "salePrice": 199,
                            "startAt": "2017-06-02T00:00:00Z",
                            "endAt": "2017-10-31T00:00:00Z"
                        }
                    ],
                    "options": [
                        {
                            "k": "Size",
                            "v": "FREE"
                        },
                        {
                            "k": "Color",
                            "v": "(16)L/Grey"
                        }
                    ]
                }
            }
        ],
        "status": "created",
        "suggests": [
            {
                "name": "EERA72505 Bundle Sale",
                "desc": "",
                "listPrice": 796,
                "salePrice": 600,
                "startAt": "2017-04-13T11:32:47Z",
                "endAt": "2017-05-13T11:32:47Z",
                "channelName": "北京汉光",
                "virtualContents": [
                    {
                        "code": "EERA72505R",
                        "listPrice": 498,
                        "salePrice": 400
                    },
                    {
                        "code": "EERA72505B",
                        "listPrice": 298,
                        "salePrice": 200
                    }
                ]
            }
        ],
        "createdAt": "2017-07-20T11:07:20Z",
        "updatedAt": "2017-07-20T11:07:21Z"
    },
    "success": true,
    "error": {}
}
```

## Create cart

`/cart/create-cart`

#### Parameters

None

#### Example

`pp://staging/cart/create-cart`

---


## Add item to cart

`/cart/add-item`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|string|
|skuId|Yes|number|
|quantity|Yes|number|
|offerId|No|number|

#### Example


`pp://staging/cart/add-item?cartId=1349&skuId=502&quantity=2&offerId=1928`

---


## Remove item from cart

`/cart/remove-item`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|string|
|skuId|Yes|number|
|quantity|Yes|number|
|offerId|No|number|

#### Example

`pp://staging/cart/remove-item?cartId=1349&skuId=184184&quantity=1&offerId=8`

---

## Change item offer

`/cart/edit-item`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|string|
|itemId|Yes|string|
|offerId|Yes|number|

#### Example

`pp://staging/cart/edit-item?cartId=1349&itemId=4638&offerId=0`

---

## Set customer

`/cart/set-customer`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|string|
|no|Yes|string|

#### Example

`pp://staging/cart/set-customer?cartId=1349&no=EE0000053147`


## Set coupon

 
`/cart/set-coupon`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|string|
|no|Yes|string|

#### Example


`pp://staging/cart/set-coupon?cartId=1349&no=EE4EEDE03E762A2AA2`


## Set info
 
`/cart/set-info`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|string|
|`key`|Yes|string|

#### Example

`pp://staging/cart/set-info?cartId=326&receipt=193018485875930103&casher=nancy`


## Use mileage

`/cart/use-mileage`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|string|
|amount|Yes|number|

#### Example

`pp://staging/cart/use-mileage?cartId=1349&amount=208`


## Set payment

 
`/cart/set-payment`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|string|
|method|Yes|string|
|amount|Yes|number|

#### Example

`pp://staging/cart/set-payment?cartId=1349&method=alipay&amount=690`

## Remove cart

`/cart/remove-cart`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|string|

#### Example

`pp://staging/cart/remove-cart?cartId=1349`


---


## Get all carts

`/cart/all-carts`

#### Parameters

None

#### Example


`pp://staging/cart/all-carts`

---


## Get cart

`/cart/get-cart`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|string|

#### Example

`pp://staging/cart/get-cart?cartId=1349`


## Set salesman

 
`/cart/set-salesman`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|string|
|salesmanId|Yes|number|

#### Example

`pp://staging/cart/set-salesman?cartId=1349&salesmanId=58`

## Clear cart

 
`/cart/clear-cart`

#### Parameters

|Name|Required|Type|
|---|---|---|
|cartId|Yes|string|

#### Example

`pp://staging/cart/clear-cart?cartId=1349`
