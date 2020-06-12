---
title: 【从0开始搭建个人博客】自建服务器，搭建一个typecho博客
top: true
categories:
  - 网站推荐
copyright: true
abbrlink: 297150169
date: 2020-06-05 13:09:18
tags:
toc_number:
toc:
top_img:
cover: https://imgkr.cn-bj.ufileos.com/fe389104-e942-4c46-8810-f9a6ae1bb7b0.png
description:
keywords:
---


上一篇讲了域名购买和服务器的选择。

现在，服务器买好了，域名也完成了解析，是时候开始主线任务——自建博客了。

首先我们先在服务上面安装一个[宝塔面板](https://www.bt.cn/)，对于linux基础不是很好的小伙伴们来说，这是一个很友好的图形化管理服务器的软件。

> 面板的安装教程可以参见官网，这里不展开。一行代码，2分钟能装好。


下载好宝塔面板之后，第一次登陆会让你下载LNMP或者LAMP,建议下载LNMP就行。（这里会稍微花一点时间）


装好之后，我们进入正题。

点击“软件商店”，

![](https://imgkr.cn-bj.ufileos.com/b54c0ff1-29cc-4a24-977b-a4b537e8a222.png)

选择“宝塔一键部署源码”




![](https://imgkr.cn-bj.ufileos.com/2b8ced19-91a7-47cb-8c38-34cad324dff2.png)


在博客一栏下找到typecho,点击“一键部署”

![](https://imgkr.cn-bj.ufileos.com/d61ded03-4ae3-48a2-9799-b5ada868a870.png)


这个时候，填入你希望以后别人访问你博客输入的域名，建议`blog.xxxx.com`这种，或者直接填`xxxx.com`也行。

![](https://imgkr.cn-bj.ufileos.com/6a07a1b9-948d-4357-891c-3f24251b7e86.png)

记得选择创建数据库，php版本的话默认就行。


![成功安装](https://imgkr.cn-bj.ufileos.com/7eb7446a-462d-4829-a5a4-93a06557412b.png)

点击访问站点，进行typecho安装。

![](https://imgkr.cn-bj.ufileos.com/43391fcd-09af-454b-8728-fd62fd632a14.png)


数据库名、数据库用户名、密码就是刚刚弹出的那个小窗里的内容。

![](https://imgkr.cn-bj.ufileos.com/ed35a6a4-5cd6-418b-8d4e-bc5457ef77c5.png)


用户名、登陆密码、邮箱，是指你博客登陆的信息。

![](https://imgkr.cn-bj.ufileos.com/aeeebaab-ed4b-4240-be45-2cbe8add8efe.png)

确认安装，很快就能安装好了。

![](https://imgkr.cn-bj.ufileos.com/85e39cac-40f5-47f6-95c7-213f4c0ab1bb.png)

点击直接开始使用。

![](https://imgkr.cn-bj.ufileos.com/8c82425a-df7d-49dd-99c7-23a5513c204d.png)

现在进入的就是你的博客后台，点击“网站”。

![](https://imgkr.cn-bj.ufileos.com/d135157f-fdb1-4f9a-a96d-43b4ceecdced.png)

ok，博客已经搭建完成了，大家都可以通过你这个域名访问到你的网站了。

![](https://imgkr.cn-bj.ufileos.com/e5c5172c-2a04-441f-9256-be9656891796.png)

### 设置SSL和伪静态


注意到现在我们的网站域名前面有个“不安全”的标识，把网站复制下来会发现，我们是http前缀的，并不是https。https是数据加密传输的，安全性会高一些，下面我们利用宝塔面板来给网站安装免费的SSL证书，让网站变成https，前面加上个小锁。


点击宝塔面板左侧的“网站”，选择我们自己这个域名的文件夹，点击“设置”。

![](https://imgkr.cn-bj.ufileos.com/b6f6f53e-458d-44e9-b892-51693cf88887.png)

这边的域名管理，如果你是直接用一级域名的，可以在填入一个
www开头的二级域名，这样，XXX.com和www.XXX.com指向的都是你的博客了。

![](https://imgkr.cn-bj.ufileos.com/e210923a-a5ba-44a1-bb00-1fd1098ea98f.png)

我们找到SSL，点第二个“let's encrypt”,打上勾，点击申请
![](https://imgkr.cn-bj.ufileos.com/85c720a4-3aa7-49de-b5ee-e4e05b622ec1.png)


![](https://imgkr.cn-bj.ufileos.com/968e2fad-4829-4f78-bb55-b6798aa4cd42.png)


申请好了，再打开右上角的“强制https”
![](https://imgkr.cn-bj.ufileos.com/3b662f7c-4377-4cdd-92da-45fa23cd1945.png)


这边还有一个知识点，把站点修改为伪静态。

#### 小知识：伪静态有利于搜索引擎抓取你的博客页面，利于seo，可以让更多的人看到你的博客。

找到`typecho`，保存就行。

![](https://imgkr.cn-bj.ufileos.com/a2222654-d8ce-4a25-9221-b6a875688b7d.png)

完成之后，到我们博客的后台,按提示修改一下站点链接。

![](https://imgkr.cn-bj.ufileos.com/83567d57-8031-40ac-9a11-47871c506347.png)


打开“设置”——“永久链接”，


![](https://imgkr.cn-bj.ufileos.com/4e09e1a8-bb01-43a3-a7cb-afbaee9bd1fa.png)


"启用"——"默认风格"(这里几种都可以尝试，不过因为后面主题的原因，我们选第一个)，保存。

![](https://imgkr.cn-bj.ufileos.com/864234c4-4afa-45d6-83f6-dc1a0f850eca.png)

出现这个提示，点选上。继续保存。


![](https://imgkr.cn-bj.ufileos.com/03bb7d5d-6fb5-474f-b8e2-229ba0e1c70e.png)


再次进入网站，小锁图标出现了。


![](https://imgkr.cn-bj.ufileos.com/3fcaa568-cbae-45a7-8d84-ab92b50ee19d.png)


点击我们默认生成的“hello word”文章，发现网址后缀变成了`archives/1/`

##### 小知识：这里的1就是文章的cid，后面会用到。

![](https://imgkr.cn-bj.ufileos.com/d338ebaa-e12f-4544-bd9a-f59c416d369d.png)

### 更换默认主题


回到后台控制台首页，点击更改外观。


![](https://imgkr.cn-bj.ufileos.com/7e534f6a-95d6-4a89-8ece-449ce2e9d5eb.png)


因为我们没有安装任何新的主题，所以只显示了一个默认主题


![](https://imgkr.cn-bj.ufileos.com/5c0fda63-2fa6-4796-b983-fa7ac76a6e0e.png)


回到宝塔面板，进入我们网址的根目录。

![](https://imgkr.cn-bj.ufileos.com/4d9a9a4c-213a-46ba-b6b8-0e6bcc4dc6c9.png)

找到`themes`主题文件夹。

![](https://imgkr.cn-bj.ufileos.com/4abffd35-50f2-46f0-a3b4-dc63e2fc9721.png)


上传给大家准备的新的主题模板（可以在公众号后台回复“Akina”获取）


![](https://imgkr.cn-bj.ufileos.com/32f9e184-4eef-4d70-9a26-36925afcb883.png)

点击"解压",按下面几幅图操作：

![](https://imgkr.cn-bj.ufileos.com/654e78ef-4fe2-4a3d-a08f-e393ea63b63d.png)


![](https://imgkr.cn-bj.ufileos.com/cb58fae4-d7f3-4183-8952-4641b180df8f.png)


![剪切](https://imgkr.cn-bj.ufileos.com/7c8614a7-8ac6-4bf7-8771-8516996e9227.png)


![粘贴](https://imgkr.cn-bj.ufileos.com/8bc9df10-b02c-4531-8b08-b78b0fb10f0d.png)


回到后台，再点击“更改外观”


![](https://imgkr.cn-bj.ufileos.com/4aa3d729-ecd8-4e41-8440-e6c888c11966.png)

新主题已经出现了。新主题的具体使用方法，可以参考主题开发同学的博客——[纸盒博客](https://zhebk.cn/Web/Akina.html)

这里，我们点击“启用”。

![](https://imgkr.cn-bj.ufileos.com/2ffc894c-67d6-408d-93f9-3d733468f3a4.png)

再访问我们的网址，主题已经更改成功了！

![](https://imgkr.cn-bj.ufileos.com/aa2ac33b-17d7-4800-b06f-faca6eb95ec0.png)


![](https://imgkr.cn-bj.ufileos.com/fe389104-e942-4c46-8810-f9a6ae1bb7b0.png)


![](https://imgkr.cn-bj.ufileos.com/f7cae3ff-0f8c-46d6-9967-b379d1fed283.png)


### 设置评论回复邮件提醒



找到博客里的“hello world”文章，打开，点击“查看沙发”


![](https://imgkr.cn-bj.ufileos.com/f8c9bedf-90f1-4874-a382-a475dbe12437.png)

这边就是评论区了。

![](https://imgkr.cn-bj.ufileos.com/b84de64a-8276-443e-bfd7-d25e25d07a17.png)

如果博客有人给我们留言，我们是无法第一时间知道并回复的，所以，寒泥大佬写了一个可以邮件提醒的插件（和主题文件一样整理放在公众号里了，回复“邮件评论插件”获取。）

一样的方法，找到`plugins`文件夹，上传——解压。

![](https://imgkr.cn-bj.ufileos.com/35e89f6c-06b3-40c9-9dd1-fe28e9e0d6f6.png)



![](https://imgkr.cn-bj.ufileos.com/6d7f75eb-2baa-4109-aa18-930ae578b193.png)


![](https://imgkr.cn-bj.ufileos.com/6d5368d0-b70d-485a-9b40-6429d3b6f031.png)



回到后台，插件这栏已经有刚刚安装的`Comment2Mail`了。

![](https://imgkr.cn-bj.ufileos.com/a3b7bba4-955c-4abf-a5e9-742eaaaad2ba.png)


![点击启用](https://imgkr.cn-bj.ufileos.com/181cc4b2-06a3-4202-b202-17f0b62bcd12.png)


![点击设置](https://imgkr.cn-bj.ufileos.com/0ef0ff26-130f-4aea-8992-50b3f736a8a4.png)


进入设置页面，其他的都比较简单，按照图里内容来填写就行


![](https://imgkr.cn-bj.ufileos.com/6668caac-5837-40d6-9ffa-97261c4bc47f.png)


![](https://imgkr.cn-bj.ufileos.com/6682ecd3-e659-4972-89ba-e67cbfa3666b.png)


这边我用的是qq邮箱，其他邮箱的话，自己可以百度一下。

这边的SMTP 登录密码，不是我们qq邮箱的密码，而是需要我们到邮箱里获取。


进入qq邮箱。


![](https://imgkr.cn-bj.ufileos.com/f0533f8c-ba65-4218-b8af-86a9064b65a9.png)

点击“账户”

![](https://imgkr.cn-bj.ufileos.com/cac43a71-c5bd-4a1a-ac91-2fcb5ca44621.png)

开启IMAP

![](https://imgkr.cn-bj.ufileos.com/dd03a3f5-d74a-4d62-a024-121723fd90bc.png)

这边根据提示发送短信之后，你就会收到这个邮箱的SMTP 登录密码了。

填到插件里头保存即可。

![](https://imgkr.cn-bj.ufileos.com/1a9ca049-3c1b-4ba5-bd70-a2cc6a9622a2.png)

PS:大家可以用小号留言测试一下插件是否正常工作。一般来说都是没有问题的。


### 主题简单设置


在博客后台，点击“更改外观”——“设置外观”

![](https://imgkr.cn-bj.ufileos.com/b2d960c0-d40a-4e25-b096-d0343d44588d.png)


里面按照提示设置自己的内容就行，更具体的使用方法，可以参考主题开发同学的博客——[纸盒博客](https://zhebk.cn/Web/Akina.html)

![](https://imgkr.cn-bj.ufileos.com/ceb56b14-114a-4bd4-b31d-0a3155d0a6e9.png)


唯一注意的一点，这边的cid就是前面提到的网址后面的那个数字

![](https://imgkr.cn-bj.ufileos.com/c3fabbb2-7b48-4247-8b71-44b8b032dd45.png)


![](https://imgkr.cn-bj.ufileos.com/914e053f-f96a-4f60-831e-d4f65df731b9.png)


点击——“撰写”——“撰写文章”，开始正式写自己的第一篇文章把。

![](https://imgkr.cn-bj.ufileos.com/4d9a5b5f-b409-47b0-b901-531f3b3e3c66.png)

文章还可以设置密码噢。

![](https://imgkr.cn-bj.ufileos.com/0cc28424-b10e-4a3e-914a-7e45b741cf93.png)

## Arina主题
!!!
<p>
<a id="download_link" class="download" href="https://pan.baidu.com/s/1JHUYnj_-Q8iHAbKLdxg64A  " rel="external" target="_blank" title="下载地址">  
<span><i class="iconfont icon-download"></i>点击下载</span>
</a>
</p>
!!! 
密码:swdp


## 邮件评论插件

!!!
<p>
<a id="download_link" class="download" href="https://pan.baidu.com/s/1TrCyXfIaV3JESGlkvM3dtQ  " rel="external" target="_blank" title="下载地址">  
<span><i class="iconfont icon-download"></i>点击下载</span>
</a> 
</p>
!!! 
密码:i7hv

