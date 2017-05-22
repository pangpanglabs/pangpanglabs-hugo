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

`pp://staging/catalog/search-contents?q=CD&skipCount=0&maxResultCount=10`

Success:
```
{
    "result": {
        "items": [
            {
                "id": 23,
                "code": "CD7C1B4P",
                "name": "Calvin Klein Women's Scuba Crepe Starburst Sheath Dress",
                "desc": "<p>Starburst detail</p><p>Sheath dress</p>",
                "listPrice": 89.98,
                "brandCode": "Calvin Klein",
                "offers": [
                    {
                        "id": 1928,
                        "code": "C194017",
                        "name": "VIP Sale",
                        "salePrice": 71.18,
                        "startAt": "2017-05-08T12:46:00Z",
                        "endAt": "2017-06-09T12:46:00Z",
                        "requirement": {
                            "customerGroup": "VIP"
                        }
                    },
                    {
                        "id": 1925,
                        "code": "S194014",
                        "name": "Hot Sale",
                        "salePrice": 89.98,
                        "startAt": "2017-05-08T12:46:00Z",
                        "endAt": "2017-06-09T12:46:00Z",
                        "requirement": null
                    }
                ],
                "options": {
                    "Color": [
                        "Ivy Mist",
                        "Monument",
                        "Rose Dust",
                        "Vanilla Ice"
                    ],
                    "Size": ["26","27","28","29","30","31","32","33"]
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
                        "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL.jpg",
                        "width": 385,
                        "height": 500
                    },
                    "medium": {
                        "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL._SL160_.jpg",
                        "width": 123,
                        "height": 160
                    },
                    "small": {
                        "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL._SL75_.jpg",
                        "width": 58,
                        "height": 75
                    }
                }
            },
            {
                "id": 21,
                "code": "CD7C1B4P",
                "name": "Calvin Klein Women's Scuba Crepe Starburst Sheath Dress",
                "desc": "<p>Starburst detail</p><p>Sheath dress</p>",
                "listPrice": 89.98,
                "brandCode": "Calvin Klein",
                "options": {
                    "Color": [
                        "Black",
                        "Ivy Mist",
                        "Maple Butter",
                        "Poise",
                        "Snow White"
                    ],
                    "Size": ["25","26","27","28","29","30","31","32","33"]
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
                        "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL.jpg",
                        "width": 385,
                        "height": 500
                    },
                    "medium": {
                        "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL._SL160_.jpg",
                        "width": 123,
                        "height": 160
                    },
                    "small": {
                        "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL._SL75_.jpg",
                        "width": 58,
                        "height": 75
                    }
                }
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

`pp://staging/catalog/get-content?id=23`

```
{
    "result": {
        "id": 23,
        "code": "CD7C1B4P",
        "name": "Calvin Klein Women's Scuba Crepe Starburst Sheath Dress",
        "desc": "<p>Starburst detail</p><p>Sheath dress</p>",
        "listPrice": 89.98,
        "brandCode": "Calvin Klein",
        "offers": [
            {
                "id": 1928,
                "code": "C194017",
                "name": "VIP Sale",
                "salePrice": 71.18,
                "startAt": "2017-05-08T12:46:00Z",
                "endAt": "2017-06-09T12:46:00Z",
                "requirement": {
                    "customerGroup": "VIP"
                }
            },
            {
                "id": 1925,
                "code": "S194014",
                "name": "Hot Sale",
                "salePrice": 89.98,
                "startAt": "2017-05-08T12:46:00Z",
                "endAt": "2017-06-09T12:46:00Z",
                "requirement": null
            }
        ],
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
                "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL.jpg",
                "width": 385,
                "height": 500
            },
            "medium": {
                "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL._SL160_.jpg",
                "width": 123,
                "height": 160
            },
            "small": {
                "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL._SL75_.jpg",
                "width": 58,
                "height": 75
            }
        },
        "skus": [
            {
                "id": 502,
                "contentId": 23,
                "name": "Calvin Klein Women's Scuba Crepe Starburst Sheath Dress, Blossom, 2",
                "code": "CD7C1B4P-0",
                "images": {
                    "large": {
                        "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL.jpg",
                        "width": 385,
                        "height": 500
                    },
                    "medium": {
                        "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL._SL160_.jpg",
                        "width": 123,
                        "height": 160
                    },
                    "small": {
                        "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL._SL75_.jpg",
                        "width": 58,
                        "height": 75
                    }
                },
                "options": [
                    {
                        "k": "Size",
                        "v": "2"
                    },
                    {
                        "k": "Color",
                        "v": "Blossom"
                    }
                ],
                "brandCode": "Calvin Klein",
                "contentCode": "CD7C1B4P",
                "listPrice": 89.98
            },
            {
                "id": 503,
                "contentId": 23,
                "name": "Calvin Klein Women's Scuba Crepe Starburst Sheath Dress, Cerulean, 2",
                "code": "CD7C1B4P-1",
                "images": {
                    "large": {
                        "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL.jpg",
                        "width": 385,
                        "height": 500
                    },
                    "medium": {
                        "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL._SL160_.jpg",
                        "width": 123,
                        "height": 160
                    },
                    "small": {
                        "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL._SL75_.jpg",
                        "width": 58,
                        "height": 75
                    }
                },
                "options": [
                    {
                        "k": "Size",
                        "v": "2"
                    },
                    {
                        "k": "Color",
                        "v": "Cerulean"
                    }
                ],
                "brandCode": "Calvin Klein",
                "contentCode": "CD7C1B4P",
                "listPrice": 89.98
            },
            {
                "id": 504,
                "contentId": 23,
                "name": "Calvin Klein Women's Scuba Crepe Starburst Sheath Dress, Popcorn, 2",
                "code": "CD7C1B4P-2",
                "images": {
                    "large": {
                        "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL.jpg",
                        "width": 385,
                        "height": 500
                    },
                    "medium": {
                        "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL._SL160_.jpg",
                        "width": 123,
                        "height": 160
                    },
                    "small": {
                        "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL._SL75_.jpg",
                        "width": 58,
                        "height": 75
                    }
                },
                "options": [
                    {
                        "k": "Size",
                        "v": "2"
                    },
                    {
                        "k": "Color",
                        "v": "Popcorn"
                    }
                ],
                "brandCode": "Calvin Klein",
                "contentCode": "CD7C1B4P",
                "listPrice": 89.98
            }
        ]
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

`pp://staging/catalog/search-skus?q=CD&skipCount=0&maxResultCount=10`

Success:
```
{
    "result": {
        "items": [
            {
                "id": 502,
                "contentId": 23,
                "name": "Calvin Klein Women's Scuba Crepe Starburst Sheath Dress, Blossom, 2",
                "code": "CD7C1B4P-0",
                "brandCode": "Calvin Klein",
                "contentCode": "CD7C1B4P",
                "listPrice": 89.98,
                "offers": [
                    {
                        "id": 1928,
                        "code": "C194017",
                        "name": "VIP Sale",
                        "salePrice": 71.18,
                        "startAt": "2017-05-08T12:46:00Z",
                        "endAt": "2017-06-09T12:46:00Z",
                        "requirement": {
                            "customerGroup": "VIP"
                        }
                    },
                    {
                        "id": 1925,
                        "code": "S194014",
                        "name": "Hot Sale",
                        "salePrice": 89.98,
                        "startAt": "2017-05-08T12:46:00Z",
                        "endAt": "2017-06-09T12:46:00Z",
                        "requirement": null
                    }
                ],
                "images": {
                    "large": {
                        "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL.jpg",
                        "width": 385,
                        "height": 500
                    },
                    "medium": {
                        "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL._SL160_.jpg",
                        "width": 123,
                        "height": 160
                    },
                    "small": {
                        "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL._SL75_.jpg",
                        "width": 58,
                        "height": 75
                    }
                },
                "options": [
                    {
                        "k": "Size",
                        "v": "2"
                    },
                    {
                        "k": "Color",
                        "v": "Blossom"
                    }
                ]
            },
            {
                "id": 503,
                "contentId": 23,
                "name": "Calvin Klein Women's Scuba Crepe Starburst Sheath Dress, Cerulean, 2",
                "code": "CD7C1B4P-1",
                "brandCode": "Calvin Klein",
                "contentCode": "CD7C1B4P",
                "listPrice": 89.98,
                "offers": [
                    {
                        "id": 1928,
                        "code": "C194017",
                        "name": "VIP Sale",
                        "salePrice": 71.18,
                        "startAt": "2017-05-08T12:46:00Z",
                        "endAt": "2017-06-09T12:46:00Z",
                        "requirement": {
                            "customerGroup": "VIP"
                        }
                    },
                    {
                        "id": 1925,
                        "code": "S194014",
                        "name": "Hot Sale",
                        "salePrice": 89.98,
                        "startAt": "2017-05-08T12:46:00Z",
                        "endAt": "2017-06-09T12:46:00Z",
                        "requirement": null
                    }
                ],
                "images": {
                    "large": {
                        "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL.jpg",
                        "width": 385,
                        "height": 500
                    },
                    "medium": {
                        "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL._SL160_.jpg",
                        "width": 123,
                        "height": 160
                    },
                    "small": {
                        "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL._SL75_.jpg",
                        "width": 58,
                        "height": 75
                    }
                },
                "options": [
                    {
                        "k": "Size",
                        "v": "2"
                    },
                    {
                        "k": "Color",
                        "v": "Cerulean"
                    }
                ]
            }
            /* ... */
        ],
        "totalCount": 87
    },
    "success": true,
    "error": {}
}
```

## Get sku

`/catalog/get-sku`

#### Parameters

|Name|Required|Type|Desc|
|---|---|---|---|
|id|-|number|-|
|uid|-|string|barcode number|

**Either `id` or `uid` is a required.**


#### Example

Request: 

`pp://staging/catalog/get-sku?id=502`

or 

`pp://staging/catalog/get-sku?uid=0888380454565`

Success:

```
{
    "result": {
        "id": 502,
        "contentId": 23,
        "name": "Calvin Klein Women's Scuba Crepe Starburst Sheath Dress, Blossom, 2",
        "code": "CD7C1B4P-0",
        "brandCode": "Calvin Klein",
        "contentCode": "CD7C1B4P",
        "listPrice": 89.98,
        "offers": [
            {
                "id": 1928,
                "code": "C194017",
                "name": "VIP Sale",
                "salePrice": 71.18,
                "startAt": "2017-05-08T12:46:00Z",
                "endAt": "2017-06-09T12:46:00Z",
                "requirement": {
                    "customerGroup": "VIP"
                }
            },
            {
                "id": 1925,
                "code": "S194014",
                "name": "Hot Sale",
                "salePrice": 89.98,
                "startAt": "2017-05-08T12:46:00Z",
                "endAt": "2017-06-09T12:46:00Z",
                "requirement": null
            }
        ],
        "images": {
            "large": {
                "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL.jpg",
                "width": 385,
                "height": 500
            },
            "medium": {
                "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL._SL160_.jpg",
                "width": 123,
                "height": 160
            },
            "small": {
                "url": "https://images-na.ssl-images-amazon.com/images/I/31ks25FUmyL._SL75_.jpg",
                "width": 58,
                "height": 75
            }
        },
        "options": [
            {
                "k": "Size",
                "v": "2"
            },
            {
                "k": "Color",
                "v": "Blossom"
            }
        ]
    },
    "success": true,
    "error": {}
}
```
