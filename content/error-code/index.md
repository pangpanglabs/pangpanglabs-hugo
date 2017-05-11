+++
title = "Error Code Description"
weight = 0
icon = "<b>5. </b>"
toc = true
+++


## System

|Code|Description|
|---|---|
|100|UknownError|
|101|Pos is not initialized.|
|102|Host name is not set. use `staging` or `production`|
|103|Host name:`{host}` is not supported|
|104|Cannot access to database file. Please check the pos-init process.|
|105|Not Found. `{path}` is not defined path.|
|106|Remote Call failed.|
|107|`{name}` is required parameter.|
|108|Invalid parameter|
|109|Network Error|

## Account

|Code|Description|
|---|---|
|200|Not authorized.|
|201|Login Failed.|
|202|Cannot get current user.|
|203|Cannot get settings.|
|204|Cannot save account to session storage.|
|205|Current Spot is not set.|
|206|Cannot set current spot.|

## Catalog

|Code|Description|
|---|---|
|300|Cannot search products.|
|301|Cannot get the product(`{uid}`).|
|302|Cannot download products.|
|303|Product(`{uid}`) is not found.|

## Cart

|Code|Description|
|---|---|
|400|Cannot find the cart(`{id}`).|
|401|Cannot add item to current cart.|
|402|Cannot remove item from current cart.|
|403|Cannot calculate current cart.|
|404|Cannot create cart.|
|405|Cannot remove current cart.|
|406|Cannot save current cart.|
|407|Cannot set customer.|
|408|Cannot set coupon.|
|409|Coupon is invalid.|
|410|Cannot set info.|
|411|Cannot set payment.|
|412|Cannot set salesman.|

## Order

|Code|Description|
|---|---|
|500|Cannot create order.|
|501|Cannot get orders.|
|502|Cannot find the order(`{id}`).|
|503|Cannot return the order(`{id}`).|
