+++
title = "Android"
weight = 1
+++

1. Set Permission in `AndroidManifest.xml` file
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

4. Call API
```
String result = Pos.call("pp://staging/account/login?tenant=LABS&username=salesman&password=1234");
```

> ### Setting
>
> #### Download
>  - Current(v0.1.0)
>  {{% button href="http://possdk.oss-cn-hangzhou.aliyuncs.com/0.1.0/pos.aar" icon="fa fa-cloud-download" %}}pos.aar{{% /button %}}
>  - 0.0.7
>  {{% button href="http://possdk.oss-cn-hangzhou.aliyuncs.com/0.0.7/pos.aar" icon="fa fa-cloud-download" %}}pos.aar{{% /button %}}
>  - v0.0.6
>  {{% button href="http://possdk.oss-cn-hangzhou.aliyuncs.com/0.0.6/pos.aar" icon="fa fa-cloud-download" %}}pos.aar{{% /button %}}
>  - v0.0.5
>  {{% button href="http://possdk.oss-cn-hangzhou.aliyuncs.com/0.0.5/pos.aar" icon="fa fa-cloud-download" %}}pos.aar{{% /button %}}
>  - v0.0.4
>  {{% button href="http://possdk.oss-cn-hangzhou.aliyuncs.com/0.0.4/pos.aar" icon="fa fa-cloud-download" %}}pos.aar{{% /button %}}
>  - v0.0.3
>  {{% button href="http://possdk.oss-cn-hangzhou.aliyuncs.com/0.0.3/pos.aar" icon="fa fa-cloud-download" %}}pos.aar{{% /button %}}
>  - v0.0.2
>  {{% button href="http://possdk.oss-cn-hangzhou.aliyuncs.com/0.0.2/pos.aar" icon="fa fa-cloud-download" %}}pos.aar{{% /button %}}
>
> #### In Project Structure
> 
> 1. click `+` 
> 2. select `import .JAR/.AAR Package`
> 3. click `Next`
> 4. select `pos.aar` file
> 5. click `Finish`
> 6. click `OK` and re-open `Project Structure`
> 7. select `app` modules
> 8. select `Dependencies` tab
> 9. click `+` button
> 10. select `3. Module Dependency`
> 11. select `possdk`
> 12. click `OK`
