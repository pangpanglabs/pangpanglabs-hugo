+++
title = "iOS"
weight = 2
+++

### Swift

1. Import
```
import Pos
```

2. Init
```
let path = NSSearchPathForDirectoriesInDomains(.libraryDirectory, .userDomainMask, true)[0]
P2PosInit(path)
```

3. Call API
```
let result = P2PosCall("pp:///account/login?username=username&password=password")
```

### Objective-C

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

3. Call API
```
NSString* result = P2PosCall(@"pp:///account/login?username=username&password=password");
```

> ### Setting
> 
> 1. Download {{% button href="http://possdk.oss-cn-hangzhou.aliyuncs.com/Pos.framework.zip" icon="fa fa-cloud-download" %}}Pos.framework.zip{{% /button %}}
> 2. Extract.
> 3. Drag and Drop `Pos.framework` file
> 4. in `Project`->`Target`->`Build Settings`  
>    Search `Enable Bitcode`  
>    set `NO`
