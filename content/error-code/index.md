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
|102|Service handler for `{path}` is not defined.|
|103|Remote Call failed.|
|104|Cannot access to database file. Please check the pos-init process.|
|105|`{name}` is required parameter.|
|106|Invalid parameter|

## Context

|Code|Description|
|---|---|
|200|Authentication is success. But cannot save account to session storage.|
|201|Login Failed.|
|202|Cannot get current user.|
|203|Cannot get settings.|
|204|Not authorized.|

## Catalog

|Code|Description|
|---|---|
|300|Cannot search products.|
|301|Cannot search contents.|
|302|Cannot find product.|

## Cart

|Code|Description|
|---|---|
|400|Cannot find cart.|
|401|Cannot add item to current cart.|
|402|Cannot remove item from current cart.|
|403|Cannot calculate current cart.|
|404|Cannot create cart.|
|405|Cannot remove current cart.|

## Order

|Code|Description|
|---|---|
|500|Cannot create order.|
|501|Cannot query orders.|
