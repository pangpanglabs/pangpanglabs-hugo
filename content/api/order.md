+++
title = "Order"
weight = 5
toc = true
+++


## Place order

`/v1/order/place-order`

#### Parameters


|Name|Required|Type|
|---|---|---|
|cartId|Yes|number|
|info|No|string(json)|

#### Example

Request: 

`pp:///v1/order/place-order?cartId=2&info=%7B%22payment%22%3A%22wxpay%22%2C%22customer%22%3A%7B%22id%22%3A2817391%2C%22mileage%22%3A150%7D%7D`

Success:
```
{
  "result": {
    "id": "d934e8b1-7b5c-48d3-92a9-6c448367d1c3",
    "orderNo": "",
    "orderType": 1,
    "subTotal": 0,
    "discountAmount": 0,
    "total": 0,
    "items": [
      {
        "skuId": 12,
        "contentId": 12,
        "quantity": 2,
        "unitPrice": 54.99,
        "subTotal": 109.98,
        "discountAmount": 0,
        "total": 109.98
      }
    ],
    "userId": 0,
    "deviceId": "aeb6b787-bf97-4305-973f-dffd8c09679b",
    "spotId": 0,
    "tenantId": 0,
    "createdAt": "2017-01-08T13:11:34.720003916Z",
    "info": {
      "customer": {
        "id": 2817391,
        "mileage": 150
      },
      "payment": "wxpay"
    }
  },
  "success": true,
  "error": {}
}
```
