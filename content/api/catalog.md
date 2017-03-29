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

## Search contents

`/catalog/search-contents`

#### Parameters

|Name|Required|Type|
|---|---|---|
|q|No|string|
|skipCount|No|number|
|maxResultCount|No|number|

#### Example

Request: 

`pp://staging/catalog/search-contents?q=42&skipCount=0&maxResultCount=10`

Success:
```
{
    "result": {
        "items": [
            {
                "id": 10,
                "code": "42AB600",
                "name": "Calvin Klein Jeans Women's Garment Dyed Ankle Skinny Pant",
                "desc": "<p>Mid-rise - sits below natural waist - skinny fit. Through hip and thigh - super skinny at ankle. Through waist, hip and thigh - skinny at ankle</p><p>Five-pocket styling with signature omega stitch on back pocket.</p><p>Zip fly with button closure</p><",
                "listPrice": 69.5,
                "salePrice": 69.5,
                "lowestPrice": 0,
                "highestPrice": 0,
                "brandCode": "Calvin Klein",
                "options": {
                    "Color": [
                        "Ivy Mist",
                        "Monument",
                        "Rose Dust",
                        "Vanilla Ice"
                    ],
                    "Size": ["26", "27", "28", "29", "30", "31", "32", "33"]
                },
                "attributes": [
                    {
                        "k": "ProductGroup",
                        "v": "Apparel"
                    },
                    {
                        "k": "ProductType",
                        "v": "PANTS"
                    },
                    {
                        "k": "Department",
                        "v": "womens"
                    }
                ],
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
                "skus": null,
                "channelInfos": null,
                "tags": null
            },
            {
                "id": 13,
                "code": "42AB616",
                "name": "Calvin Klein Jeans Women's Utility Short",
                "desc": "<p>These utility shorts are comfortable and stylish. They pair well with a Calvin Klein tee for a modern look</p><p>Inseam: 3.5 inch</p><p>Features large front and back utility pockets which give this short a fashionable look</p><p>Button fly with zip clo",
                "listPrice": 49.5,
                "salePrice": 49.5,
                "lowestPrice": 0,
                "highestPrice": 0,
                "brandCode": "Calvin Klein",
                "options": {
                    "Color": [
                        "Black",
                        "Ivy Mist",
                        "Maple Butter",
                        "Poise",
                        "Snow White"
                    ],
                    "Size": ["25", "26", "27", "28", "29", "30", "31", "32", "33"]
                    ]
                },
                "attributes": [
                    {
                        "k": "ProductGroup",
                        "v": "Apparel"
                    },
                    {
                        "k": "ProductType",
                        "v": "SHORTS"
                    },
                    {
                        "k": "Department",
                        "v": "womens"
                    }
                ],
                "images": {
                    "large": {
                        "url": "https://images-na.ssl-images-amazon.com/images/I/41oEs6gO5BL.jpg",
                        "width": 385,
                        "height": 500
                    },
                    "medium": {
                        "url": "https://images-na.ssl-images-amazon.com/images/I/41oEs6gO5BL._SL160_.jpg",
                        "width": 123,
                        "height": 160
                    },
                    "small": {
                        "url": "https://images-na.ssl-images-amazon.com/images/I/41oEs6gO5BL._SL75_.jpg",
                        "width": 58,
                        "height": 75
                    }
                },
                "skus": null,
                "channelInfos": null,
                "tags": null
            }
        ],
        "totalCount": 2
    },
    "success": true,
    "error": {}
}
```

## Get content

`/catalog/get-content`

#### Parameters

|Name|Required|Type|
|---|---|---|
|id|Yes|number|

#### Example

Request: 

`pp://staging/catalog/get-content?id=10`

```
{
  "result": {
    "id": 10,
    "code": "42AB600",
    "name": "Calvin Klein Jeans Women's Garment Dyed Ankle Skinny Pant",
    "desc": "<p>Mid-rise - sits below natural waist - skinny fit. Through hip and thigh - super skinny at ankle. Through waist, hip and thigh - skinny at ankle</p><p>Five-pocket styling with signature omega stitch on back pocket.</p><p>Zip fly with button closure</p><",
    "listPrice": 69.5,
    "salePrice": 69.5,
    "lowestPrice": 0,
    "highestPrice": 0,
    "brandCode": "Calvin Klein",
    "options": {
      "Color": [
        "Ivy Mist",
        "Monument",
        "Rose Dust",
        "Vanilla Ice"
      ],
      "Size": ["26", "27", "28", "29", "30", "31", "32", "33"]
    },
    "attributes": [
      {
        "k": "ProductGroup",
        "v": "Apparel"
      },
      {
        "k": "ProductType",
        "v": "PANTS"
      },
      {
        "k": "Department",
        "v": "womens"
      }
    ],
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
    "skus": [
      {
        "id": 168,
        "contentId": 10,
        "name": "Calvin Klein Jeans Women's Gmt Dyed Ankle Skinny Pant, Ivy Mist, 26",
        "code": "42AB600-0",
        "listPrice": 69.5,
        "salePrice": 69.5,
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
            "v": "Ivy Mist"
          }
        ],
        "uids": [
          {
            "id": 107,
            "skuId": 168,
            "idType": "EAN",
            "uid": "0637865273456"
          },
          {
            "id": 108,
            "skuId": 168,
            "idType": "UPC",
            "uid": "637865273456"
          }
        ]
      },
      /* ... sku ... */      
    ],
    "channelInfos": null,
    "tags": null
  },
  "success": true,
  "error": {}
}
```

## Search skus

`/catalog/search-skus`

#### Parameters

|Name|Required|Type|
|---|---|---|
|q|No|string|
|skipCount|No|number|
|maxResultCount|No|number|

#### Example

Request: 

`pp://staging/catalog/search-skus?q=42&skipCount=0&maxResultCount=10`

Success:
```
{
    "result": {
        "items": [
            {
                "id": 168,
                "contentId": 10,
                "name": "Calvin Klein Jeans Women's Gmt Dyed Ankle Skinny Pant, Ivy Mist, 26",
                "code": "42AB600-0",
                "listPrice": 69.5,
                "salePrice": 69.5,
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
                        "v": "Ivy Mist"
                    }
                ]
            },
            {
                "id": 169,
                "contentId": 10,
                "name": "Calvin Klein Jeans Women's Gmt Dyed Ankle Skinny Pant, Monument, 26",
                "code": "42AB600-1",
                "listPrice": 69.5,
                "salePrice": 69.5,
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
            }
        ],
        "totalCount": 76
    },
    "success": true,
    "error": {}
}
```

## [Deprecated]~~Search products~~

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
