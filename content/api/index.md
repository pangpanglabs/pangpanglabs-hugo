+++
title = "API Description"
weight = 0
icon = "<b>3. </b>"
toc = true
+++

![PangPang POS](/images/sdk.png)


## How to Initialize SDK

PosSDK use local database. When initializing, you have to send the path where the database file will be stored.

#### Android

1. For using network, Android require extra permissions.  
  Set Permission in `AndroidManifest.xml` file
```
<uses-permission android:name="android.permission.INTERNET" />
```

2. Import
```
import cn.p2shop.pos.Pos;
```

3. Init 
```
String path;
if (android.os.Build.VERSION.SDK_INT >=android.os.Build.VERSION_CODES.LOLLIPOP){
        path = getNoBackupFilesDir().getAbsolutePath();
} else{
        path = getFilesDir().getAbsolutePath();
}
Pos.init(path);
```


#### iOS

##### Swift

1. Import
```
import Pos
```

2. Init
```
let path = NSSearchPathForDirectoriesInDomains(.libraryDirectory, .userDomainMask, true)[0]
P2PosInit(path)
```

##### Objective-C

1. Import
```
#import <Pos/Pos.h>
```

2. Init
```
NSString* path = [NSSearchPathForDirectoriesInDomains(NSLibraryDirectory,
                                                          NSUserDomainMask,
                                                          YES) objectAtIndex:0];
P2PosInit(path);
```

---

## How to use SDK features

After initializing, you can use all features.
All features are definded in **uri format** and all results are **json string**.

The features are described in child pages.

- [Account](/api/account)
- [Context](/api/context)
- [Catalog](/api/catalog)
- [Cart](/api/cart)
- [Order](/api/order)


This is json response format. All json data should have 3 properties - `success`, `result`, `error`.
```
{
  success: true, /* true or false */
  result: {},    /* actual result of api */
  error: {}      /* error information */
}
```

You can call SDK features like this:

#### Android

```
String result = Pos.call("pp:///v1/account/login?tenant=LABS&username=salesman&password=1234");
```

#### iOS

##### Swift

```
let result = P2PosCall("pp:///v1/account/login?tenant=LABS&username=salesman&password=1234")
```

##### Objective-C

```
NSString* result = P2PosCall(@"pp:///v1/account/login?tenant=LABS&username=salesman&password=1234");
```
