+++
draft = true
title = "Error Code Description"
weight = 100
toc = true
+++

## System

|Code|Description|
|---|---|
|100|Pos is not initialized.|
|101|Service handler for `{path}` is not defined.|
|102|Remote Call failed.|
|103|Database Repository is null. Please check the pos-init process.|

## Account

|Code|Description|
|---|---|
|200|Authentication is success. But cannot save account to session storage.|
|201|Login Failed.|
|202|Cannot get current user from session storage.|

## Catalog

|Code|Description|
|---|---|
|300|Cannot search products from catalog storage.|
|301|Cannot search contents from catalog storage.|
|302|Cannot find product.|

## Cart

|Code|Description|
|---|---|
|400|Cannot find current cart.|
|401|Cannot add item to current cart.|
|402|Cannot calculate current cart.|
