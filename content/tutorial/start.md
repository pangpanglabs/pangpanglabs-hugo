+++
title = "Start"
weight = 1
draft = true
+++

## 1. Init

Pos SDK를 사용한 Application은 아래와 같은 방식으로 구동됩니다.

`Init` 함수를 사용해서 Pos SDK를 초기화 합니다.
Pos SDK는 로컬 파일을 사용합니다.
SDK에서 접근 가능한 로컬 파일 경로를 `Init` 함수에 인자로 전달합니다.

- iOS

```
import Pos

/* ... */

let path = NSSearchPathForDirectoriesInDomains(.libraryDirectory, .userDomainMask, true)[0]
P2PosInit(path)
```

- Android

```
import cn.p2shop.pos.Pos;

/* ... */

String path;
if (android.os.Build.VERSION.SDK_INT >=android.os.Build.VERSION_CODES.LOLLIPOP){
        path = getNoBackupFilesDir().getAbsolutePath();
} else{
        path = getFilesDir().getAbsolutePath();
}
Pos.init(path);
```

## 2. Login

로그인을 위해 `/account/login`과 `/account/autologin` 두 API를 제공합니다.

- `/account/login`  
  `username`, `password`를 파라미터로 전달하여 로그인
- `/account/autologin`  
  이전 로그인에서 발급된 token을 사용하여 로그인.  
  발급된 token이 유효한 경우 별도 로그인 절차를 거치치 않음.
  token이 만료된 경우 `/account/login`으로 다시 로그인을 해야 함.

## 3. Cart 사용

로그인이 완료되면 카트를 사용할 수 있다.

