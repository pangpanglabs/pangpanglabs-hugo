+++
title = "Cart"
weight = 4
toc = true
+++

## Cart result example

```
{
    "result": {
        "id": "3520",
        "tenantId": 4,
        "listPrice": 3588,
        "salePrice": 2511.6,
        "quantity": 4,
        "discount": 1076.4,
        "remainAmount": 1033.6,
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
        "info": {
            "receipt": "483017401830101"
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
        "items": [
            {
                "id": "4638",
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
                            "channelName": "北京汉光",
                            "startAt": "2017-05-01T00:00:00Z",
                            "endAt": "2017-06-02T00:00:00Z",
                            "requirement": {}
                        }
                    ]
                },
                "offer": {
                    "id": 1952,
                    "code": "C108097",
                    "name": "百货店vip 9折",
                    "salePrice": 538.2,
                    "channelName": "北京汉光",
                    "startAt": "2017-05-01T00:00:00Z",
                    "endAt": "2017-06-02T00:00:00Z",
                    "requirement": {}
                },
                "quantity": 2,
                "listPrice": 1196,
                "salePrice": 1076.4,
                "discount": 119.6
            },
            {
                "id": "4639",
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
                "id": "4640",
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
                            "channelName": "北京汉光",
                            "startAt": "2017-05-01T00:00:00Z",
                            "endAt": "2017-06-02T00:00:00Z",
                            "requirement": {
                                "customerGroup": "VIP"
                            }
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
        "userId": 14,
        "spotId": 26,
        "salesmanId": 3149,
        "createdAt": "2017-05-11T16:19:33Z",
        "updatedAt": "2017-05-11T16:24:19.216021056Z"
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
