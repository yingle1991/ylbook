---

layout:   post

title:   "typora和picgo使用"

subtitle:  "----程序员的博客生活"

date:    2020-11-30

tags:

  - 生活杂谈

---



## 序

Markdown是一种[轻量级标记语言](https://baike.baidu.com/item/轻量级标记语言/52671915)，创始人为约翰·格鲁伯（英语：John Gruber）。 它允许人们使用易读易写的纯文本格式编写文档，然后转换成有效的XHTML（或者HTML）文档。这种语言吸收了很多在电子邮件中已有的纯文本标记的特性，很适合我们这种技术极客博客创作使用。但是对于博客上传图片又不是很友好，于是 typora搭配picgo使用的方案应运而生。

## 1.picgo下载

下载地址[https://github.com/Molunerfinn/PicGo/releases/tag/v2.2.2]

国内github下载比较慢我放到了百度云上

下载链接: https://pan.baidu.com/s/1QtQSOR8xieXsEvjISl75UA 提取码: mi4w 

## 2.picgo码云插件

- 在picgo插件栏中搜索gitee 2.0.3插件

  ![](https://gitee.com/yingle1991/resource/raw/master/static/blog/QQ图片20201130200709.png)

- 如果插件安装报错，请[点击这里](http://nodejs.cn/download/)下载并安装Node.js

<!--more-->

## 3.设置gitee仓库

- 在gitee新建一个公开的资源仓库

  ![](https://gitee.com/yingle1991/resource/raw/master/static/blog/QQ图片20201130200836.png)

- 设置个人token

  ![](https://gitee.com/yingle1991/resource/raw/master/static/blog/QQ图片20201130200927.png)

## 4.设置picgo的gitee配置参数

repo：仓库地址去掉码云域名 https://gitee.com/yingle1991/resource

branch：主干

token：上面设置的个人token

path：是仓库中新建static文件夹

![](https://gitee.com/yingle1991/resource/raw/master/static/blog/20201130200958.png)

**点击设为默认图床，点击确定**

## 5.激活PicGo-Server

2.2.0 版本之后，**PicGo 内部会默认开启一个小型的服务器，用于配合其他应用来调用 PicGo 进行上传。**

**如何设置呢？**

打开 PicGo 详细页面，进入 **PicGo 设置–设置Server**

参考下图进行设置即可。

![](https://gitee.com/yingle1991/resource/raw/master/static/blog/QQ图片20201130201102.png)

## 6.Typora设置

### 版本要求

Typora 0.9.84 及以上。

### 设置

**文件–偏好设置–图像**

![](https://gitee.com/yingle1991/resource/raw/master/static/blog/QQ图片20201130201132.png)

参考图片中的进行配置。

选择本机 PicGo 的路径。

### 7. 验证图片上传

这里还可以**验证图片上传功能**。

验证成功会返回下图结果：

![](https://gitee.com/yingle1991/resource/raw/master/static/blog/QQ图片20201130201503.png)