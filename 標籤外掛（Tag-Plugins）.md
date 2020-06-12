---
title: 標籤外掛（Tag Plugins）
top: true
categories:
  - 网站推荐
abbrlink: 2237228359
date: 2020-06-05 17:12:55
tags:
toc_number:
toc:
top_img: 
cover: https://img2.jiemian.com/jiemian/original/20170317/148972035174084700_a580xH.jpg
description:
keywords:
copyright:
---

## Note (Bootstrap Callout)

{% note default %}
default 提示塊標籤
{% endnote %}

{% note primary no-icon %}
primary 提示塊標籤
{% endnote %}

{% note success %}
success 提示塊標籤
{% endnote %}

{% note info %}
info 提示塊標籤
{% endnote %}

{% note warning %}
warning 提示塊標籤
{% endnote %}

{% note danger %}
danger 提示塊標籤
{% endnote %}

## Gallery相冊圖庫

<div class="gallery-group-main">
{% galleryGroup '壁紙' '收藏的一些壁紙' '/Gallery/wallpaper' https://i.loli.net/2019/11/10/T7Mu8Aod3egmC4Q.png %}
{% galleryGroup '漫威' '關於漫威的圖片' '/Gallery/marvel' https://i.loli.net/2019/12/25/8t97aVlp4hgyBGu.jpg %}
{% galleryGroup 'OH MY GIRL' '關於OH MY GIRL的圖片' '/Gallery/ohmygirl' https://i.loli.net/2019/12/25/hOqbQ3BIwa6KWpo.jpg %}
</div>

## Gallery相冊

{% gallery %}
![](https://gratisography.com/wp-content/uploads/2019/10/gratisography-scary-pumpkin-hand-900x600.jpg)
![](https://gratisography.com/wp-content/uploads/2019/10/gratisography-fresh-fish-dinner-900x600.jpg)
![](https://gratisography.com/wp-content/uploads/2019/10/gratisography-mountain-cloud-landscape-900x600.jpg)
![](https://picjumbo.com/wp-content/uploads/iphone-free-stock-photos-2210x3315.jpg)
![](https://picjumbo.com/wp-content/uploads/young-millennial-girl-drinking-lemonade-and-overlooking-the-city-2210x1473.jpg)
![](https://picjumbo.com/wp-content/uploads/modern-graphic-designer-essentials_free_stock_photos_picjumbo_HNCK4919-2210x1474.jpg)
{% endgallery %}

## tag-hide

### Inline

哪個英文字母最酷？ {% hideInline 因為西裝褲(C裝酷),查看答案,#FF7242,#fff %}

門裏站着一個人? {% hideInline 閃 %}

### Block

{% hideBlock 查看答案 %}
{% gallery %}
![](https://i.loli.net/2019/12/25/Fze9jchtnyJXMHN.jpg)
![](https://i.loli.net/2019/12/25/ryLVePaqkYm4TEK.jpg)
![](https://i.loli.net/2019/12/25/gEy5Zc1Ai6VuO4N.jpg)
![](https://i.loli.net/2019/12/25/d6QHbytlSYO4FBG.jpg)
![](https://i.loli.net/2019/12/25/6nepIJ1xTgufatZ.jpg)
![](https://i.loli.net/2019/12/25/E7Jvr4eIPwUNmzq.jpg)
![](https://i.loli.net/2019/12/25/mh19anwBSWIkGlH.jpg)
![](https://i.loli.net/2019/12/25/2tu9JC8ewpBFagv.jpg)
{% endgallery %}
{% endhideBlock %}

### Toggle

{% hideToggle Butterfly安裝方法 %}
在你的博客根目錄裏

​```git
git clone -b master https://github.com/jerryc127/hexo-theme-butterfly.git themes/Butterfly
​```

如果想要安裝比較新的dev分支，可以

​```git
git clone -b dev https://github.com/jerryc127/hexo-theme-butterfly.git themes/Butterfly
​```

{% endhideToggle %}

### mermaid

{% mermaid %}
pie
    title Key elements in Product X
    "Calcium" : 42.96
    "Potassium" : 50.05
    "Magnesium" : 10.01
    "Iron" :  5
{% endmermaid %}



