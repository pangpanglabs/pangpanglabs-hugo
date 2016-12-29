+++
title = "Global Settings"
weight = 1
toc = true
+++

## System


|Code|Type|Description|Default|
|---|---|---|---|
|System.AllowOffline|boolean| |`true`|
|System.TraceInterval|integer|sending trace log to server interval(seconds)|`60`|

## ShoppingCart

|Code|Type|Description|Default|
|---|---|---|---|
|ShoppingCart.Price.RoundPoint|integer| |`2`|
|ShoppingCart.Price.RoundStrategy|string|`"floor"`round down <br /> `"ceil"`: round up <br /> `"round"`: round to the nearest integer |`"round"`|
|ShoppingCart.Price.Culture|string|`"USD"`($), `"EUR"`(€), `"CNY"`(¥), `"KRW"`(₩) |`"CNY"`|
|ShoppingCart.Payment|string array|`"alipay"`, `"wxpay"`, `"cash"`|`["alipay", "wxpay"]`|


