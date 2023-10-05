---
title: draft and future post
subtitle: jekyll 的草稿 與 預先發文
excerpt: A demo page checking Chulapa jekyll post demo
categories: [tutorial]
tags: [jekyll]
header_img: https://cdn.pixabay.com/photo/2023/07/19/19/14/monarch-butterfly-8137642_1280.png
---

![](https://cdn.pixabay.com/photo/2023/07/19/19/14/monarch-butterfly-8137642_1280.png)

# jekyll 的草稿 與 預先發文

------

## 草稿:

放在 `_draft` 資料夾內的檔案會被視為草稿, Jekyll 會忽略草稿, 不會公開

如果在本地伺服器想要查看, 可以使用以下指令:

~~~sh
jekyll serve --drafts 
~~~

------

## 不公開文章

在文章的 `front matter` 加上這個參數,

~~~yaml
---
published: false
---
~~~

把文章設為不公開, Jekyll 就會忽略文章

如果在本地伺服器想要查看, 可以使用以下指令:

~~~sh
jekyll serve --unpublished
~~~

------

## 排程發文

把文章的日期設定為你想排程發文的未來日期, Jekyll 會等到那個時候才發文公開

在本地伺服器想要查看, 可以使用以下指令:

~~~sh
jekyll serve --future
~~~

------

參考:
<https://jekyllrb.com/docs/posts/>
<https://www.hongkiat.com/blog/jekyll-draft/>
<https://diamantidis.github.io/tips/2020-06-13-working-with-drafts-on-jekyll-blog>

