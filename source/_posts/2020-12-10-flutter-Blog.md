---
layout:     post
title:      "登录token认证以及密码加密"
subtitle:   "---程序员的积累"
date:       2020-12-10
author:     "ZYL"
tags:
  - 技术
  - 生活
---

#### 1.登录认证



``` java
md5String 加密对象=时间戳
md5Key md5加密浴 =APITest
    
String enstr=Encrypter.encrypt(password,Encrypter.generateSign(md5String,md5Key));//传递所有密码以此方式加密传递

    
String denstr=Encrypter.decrypt(enstr,Encrypter.generateSign(md5String,md5Key));//后台所有密码以此方式解密

```
<!--more-->

```flow

st=>start: 开始

op=>operation: 对用户密码进行解密操作

cond=>condition: 判断框(是或否?)

sub1=>subroutine: 登录验证

io=>inputoutput: 返回登录用户(增加token）8小时有效

e=>end: 结束框

st->op->cond

cond(yes)->io->e

cond(no)->sub1(right)->cond

```

备注：返回token 下次访问接口需要 以Secret传递回来，8小时有效，否则返回未登录错误～

 ![关注我得到更多信息](/img/passme.png)
