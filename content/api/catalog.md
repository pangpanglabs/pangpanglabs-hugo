+++
title = "Catalog"
weight = 3
toc = true
+++



## Download products

`/catalog/download`

#### Parameters

None

#### Example

Request:

`pp://staging//catalog/download`

Success:
```
{
  "result": 0,
  "success": true,
  "error": {}
}
```


## Search products

`/catalog/search-products`

#### Parameters

|Name|Required|Type|
|---|---|---|
|q|No|string|
|skipCount|No|number|
|maxResultCount|No|number|

#### Example

Request: 

`pp://staging/catalog/search-products?q=EK&skipCount=0&maxResultCount=10`

Success:
```
{
  "result": {
    "items": [
      {
        "uid": "305228",
        "name": "EKJP6CV102, (59)Navy, (135)135",
        "listPrice": 450,
        "salePrice": 450,
        "skuCode": "EKJP6CV10259135",
        "contentCode": "EKJP6CV102",
        "brandCode": "EK"
      },
      /* ... */
      {
        "uid": "305279",
        "name": "EKAP7S111K, (25)Pink, (200)200",
        "listPrice": 398,
        "salePrice": 398,
        "skuCode": "EKAP7S111K25200",
        "contentCode": "EKAP7S111K",
        "brandCode": "EK"
      }
    ],
    "totalCount": 11939
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
