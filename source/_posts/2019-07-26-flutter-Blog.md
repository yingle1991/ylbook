---
layout:     post
title:      "如何解决android.support.v4.content.FileProvider异常错误的问题？"
subtitle:   "---工作记录"
date:       2019-07-26
author:     "ZYL"
header-img: "img/post-bg-universe.jpg"
tags:
  - flutter
  - 笔记
  - 协作开发
---


问题如下
```
Using hardware rendering with device Android SDK built for x86 64. If you get graphics artifacts, consider enabling software rendering with
"--enable-software-rendering".
Launching lib/main.dart on Android SDK built for x86 64 in debug mode...
Initializing gradle...                                              1.5s
Resolving dependencies...                                          17.3s
F:\dartSpace\flutter\Demo\salesman_field\android\app\src\main\java\com\example\salesman_field\MainActivity.java:14: ����: �����android.support.v4.
content������
import android.support.v4.content.FileProvider;
                                 ^
F:\dartSpace\flutter\Demo\salesman_field\android\app\src\main\java\com\example\salesman_field\MainActivity.java:60: ����: �����android.support.v4.
content������
               Uri uri7 = android.support.v4.content.FileProvider.getUriForFile(this,"com.example.salesman_field.android7.fileprovider", apkFile);  
                                                    ^
2 ������

FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':app:compileDebugJavaWithJavac'.
> Compilation failed; see the compiler error output for details.

* Try:
Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output. Run with --scan to get full insights.

* Get more help at https://help.gradle.org

BUILD FAILED in 46s
Running Gradle task 'assembleDebug'...
Running Gradle task 'assembleDebug'... Done                        46.8s
*******************************************************************************************
The Gradle failure may have been because of AndroidX incompatibilities in this Flutter app.
See https://goo.gl/CP92wY for more information on the problem and how to fix it.
*******************************************************************************************
Gradle task assembleDebug failed with exit code 1
PS F:\dartSpace\flutter\Demo\salesman_field> flutter run
Using hardware rendering with device Android SDK built for x86 64. If you get graphics artifacts, consider enabling software rendering with
"--enable-software-rendering".
Launching lib/main.dart on Android SDK built for x86 64 in debug mode...
Initializing gradle...                                              2.8s
Resolving dependencies...                                          33.7s
F:\dartSpace\flutter\Demo\salesman_field\android\app\src\main\java\com\example\salesman_field\MainActivity.java:61: ����: �����android.support.v4.
content������
               Uri uri7 = android.support.v4.content.FileProvider.getUriForFile(this,"com.example.salesman_field.android7.fileprovider", apkFile);  
                                                    ^
1 ������

FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':app:compileDebugJavaWithJavac'.
> Compilation failed; see the compiler error output for details.

* Try:
Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output. Run with --scan to get full insights.

* Get more help at https://help.gradle.org

BUILD FAILED in 26s
Running Gradle task 'assembleDebug'...
Running Gradle task 'assembleDebug'... Done                        27.4s
*******************************************************************************************
The Gradle failure may have been because of AndroidX incompatibilities in this Flutter app.
See https://goo.gl/CP92wY for more information on the problem and how to fix it.
*******************************************************************************************
Gradle task assembleDebug failed with exit code 1
```

为兼容24之上版本代码做了些改变报错，查阅资料

```
android.support.v4.content.FileProvider->androidx.core.content.FileProvider
````
问题解决

纯属开发笔记，有啥补充尽可联系我~
yingle1991@163.com