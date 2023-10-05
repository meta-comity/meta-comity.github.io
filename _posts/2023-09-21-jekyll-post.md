---
title: 如何設定 jekyll 的 markdown 文章
subtitle: 主要參考 chulapa 的設定
excerpt: A demo page checking Chulapa jekyll post demo
categories: [tutorial]
tags: [jekyll,chulapa]
header_img: https://cdn.pixabay.com/photo/2017/07/24/19/57/tiger-2535888_1280.jpg
---

![](https://cdn.pixabay.com/photo/2017/07/24/19/57/tiger-2535888_1280.jpg)

像這篇文章的meta-data看起來像這樣:

~~~yaml
---
title: 如何設定 jekyll 的 markdown 文章
subtitle: 主要參考 chulapa 的設定
excerpt: A demo page checking Chulapa jekyll post demo
categories: [tutorial]
tags: [jekyll,chulapa]
header_img: https://cdn.pixabay.com/photo/2017/07/24/19/57/tiger-2535888_1280.jpg
---
~~~

header_type有這些選項:
- base
- post
- hero
- image
- splash

不過文章通常不用改，我預設已經使用 post

header_img 圖片我會去免費圖庫找大圖, 然後右鍵複製影像連結

+ 免費圖庫:
  - <https://pixabay.com/>
    * 注意看一下, 有些區塊他會寫 Sponsored images iStock LIMITED DEAL 20% off with PIXABAY20 coupon  
      表示這是iStock圖片,要付費  
      主要是搜尋的時候的第一排圖片  
      以及點開大圖之後, 下面第一排圖片, 還有右邊的圖片  
      點開大圖之後要往下拉, 看到**Related free image**區塊, 才是免費圖片
  - <https://unsplash.com/>
    * unsplash 的圖片上面如果有寫 __Unsplash+__  
      表示要付費
  - <https://www.freepik.com/>
  - <https://www.shopify.com/stock-photos/>
  - <https://stocksnap.com/>

+ AI圖:
  - <https://www.bing.com/create>
  - <https://www.ipic.ai/>
  - <https://pixlr.com/tw/ai/ai-image-generator/>
  - <https://www.visme.co/ai-image-generator/>
  - <https://perchance.org/ai-photo-generator>



其他範例請參考: [chulapa demo][demo]


[demo]: https://dieghernan.github.io/chulapa/demo

