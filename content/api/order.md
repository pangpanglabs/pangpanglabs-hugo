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
    "id": "92f8c3cc-11c4-4408-8634-f5701f8f1a7c",
    "orderNo": "",
    "listPrice": 4380,
    "discount": 2124,
    "salePrice": 2256,
    "items": [
      {
        "id": 1,
        "name": "EKJP6CV102, (59)Navy, (135)135",
        "channel": "elandpos",
        "uid": "305228",
        "unitListPrice": 450,
        "unitSalePrice": 0,
        "quantity": 1,
        "listPrice": 450,
        "salePrice": 450,
        "discount": 0
      },
      {
        "id": 2,
        "name": "LONG DOWN JUMPER, (39)Ivory, X-SMALL",
        "channel": "elandpos",
        "uid": "1",
        "unitListPrice": 1290,
        "unitSalePrice": 0,
        "quantity": 2,
        "listPrice": 2580,
        "salePrice": 1806,
        "discount": 774
      }
    ],
    "createdAt": "2017-03-01T15:52:58.903324782Z",
    "couponNo": "WA976CE9199756D5BC",
    "info": {
      "payment": {
        "alipay": "150",
        "wxpay": "30"
      },
      "receipt": "193018485875930103"
    },
    "Status": 0
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
        "id": "92f8c3cc-11c4-4408-8634-f5701f8f1a7c",
        "orderNo": "",
        "listPrice": 4380,
        "discount": 2124,
        "salePrice": 2256,
        "createdAt": "2017-03-01T15:52:58Z",
        "customerID": 0,
        "couponNo": "WA976CE9199756D5BC",
        "info": {
          "payment": {
            "alipay": "150",
            "wxpay": "30"
          },
          "receipt": "193018485875930103"
        },
        "Status": 1
      },
      {
        "id": "fee5af93-e2db-4ee7-8c70-b179a2054f14",
        "orderNo": "",
        "listPrice": 1090,
        "discount": 0,
        "salePrice": 1090,
        "createdAt": "2017-03-01T15:55:59Z",
        "customerID": 1,
        "couponNo": "",
        "info": null,
        "Status": 1
      }
    ],
    "totalCount": 2
  },
  "success": true,
  "error": {}
}
```
