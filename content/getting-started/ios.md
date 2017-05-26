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
let result = P2PosCall("pp://staging/account/login?tenant=LABS&username=salesman&password=1234")
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
NSString* result = P2PosCall(@"pp://staging/account/login?tenant=LABS&username=salesman&password=1234");
```

> ### Setting
>
> #### Download
>  - Current(v0.1.1)
>  {{% button href="http://possdk.oss-cn-hangzhou.aliyuncs.com/0.1.1/Pos.framework.zip" icon="fa fa-cloud-download" %}}Pos.framework.zip{{% /button %}}
>
>  - Archived versions
>  {{% button href="https://pangpanglabs.github.io/introduction/#archived-versions" icon="fa fa-external-link" %}}click{{% /button %}}
>
> #### Project Setting
>
> 1. Extract `Pos.framework.zip` file.
> 2. Drag and Drop `Pos.framework` to Xcode project.
> 3. in `Project`->`Target`->`Build Settings`  
>    - Search `Enable Bitcode`  
>    - set `NO`
