+++
title = "Catalog"
weight = 3
toc = true
+++


## Search products

`/v1/catalog/search-products`

#### Parameters

|Name|Required|Type|
|---|---|---|
|q|No|string|
|skipCount|No|number|
|maxResultCount|No|number|

#### Example

Request: 

`pp:///v1/catalog/search-products?q=A&skipCount=0&maxResultCount=10`

Success:
```
{
  "result": {
    "items": [
      {
        "skuId": 4,
        "skuCode": "AP_MBP_13_1",
        "contentId": 4,
        "name": "Apple MacBook Pro 13-inch",
        "price": 1800
      },
      {
        "skuId": 5,
        "skuCode": "AS_551_LP_1",
        "contentId": 5,
        "name": "Asus N551JK-XO076H Laptop",
        "price": 1500
      },
      {
        "skuId": 10,
        "skuCode": "AD_CS4_PH_1",
        "contentId": 10,
        "name": "Adobe Photoshop CS4",
        "price": 75
      },
      {
        "skuId": 17,
        "skuCode": "APPLE_CAM_1",
        "contentId": 17,
        "name": "Apple iCam",
        "price": 1300
      },
      {
        "skuId": 25,
        "skuCode": "AD_C80_RS_1",
        "contentId": 25,
        "name": "adidas Consortium Campus 80s Running Shoes",
        "price": 27.56
      }
    ],
    "totalCount": 5
  },
  "success": true,
  "error": {}
}
```

Fail:

```
{
  "success": false,
  "error": {
    "code": 300,
    "message": "Cannot search products."
  }
}
```
