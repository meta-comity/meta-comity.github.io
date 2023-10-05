---
title: 如何使用Markdown/Kramdown語法寫文章
subtitle: Markdown/Kramdown語法簡單介紹
tags: [markdown,kramdown]
header_img: https://cdn.pixabay.com/photo/2023/09/04/13/17/mushrooms-8232731_1280.jpg
---

![](https://cdn.pixabay.com/photo/2023/09/04/13/17/mushrooms-8232731_1280.jpg)

目錄 TOC (Table Of Contene)

* 此行是必需的，但不會出現。將 '*' 替換為 '1' 以建立編號清單。
{:toc}

# Markdown/Kramdown 是什麼？

![markdown](/assets/markdown.png){:height="48px" width="36px"}

## Markdown

![markdown](/assets/markdown.png)

> [!NOTE]  
> markdown不能加圖片說明文字,可以自己打在下一行

### 簡介

Markdown 是一種 **[輕量級標記語言][輕量級標記語言定義]**，
可用於為__純文字文件新增格式元素__。

Markdown 由 **[John Gruber][John Gruber資訊]** 於 2004 年創建，
現已成為世界上最受歡迎的標記語言之一。


[輕量級標記語言定義]: https://zh.wikipedia.org/zh-tw/輕量級標記語言 （英語：Lightweight Markup Language，簡稱LML）是一類用簡單句法描述簡單格式的文本語言。
[John Gruber資訊]: https://daringfireball.net/projects/markdown/

### 特性

根據 [維基百科][markdown維基百科]

[markdown維基百科]: https://zh.wikipedia.org/zh-tw/Markdown

由於Markdown:
1. 輕量化
2. 易讀
3. 易寫
4. 並且支援:
  + 圖片
  * 圖表
  - Latex數學公式
    - 似乎有些瀏覽器不支援顯示 Latex,  
      ~~比如說手機版的 Google Chrome~~

目前許多網站都廣泛使用Markdown:
- 撰寫說明文件,  
  比如說 Github
- 用於論壇上發表訊息  
  比如說 Discord

*[Github] 最多人使用的 git 版本管理倉庫遠端託管平臺

*[Discord] 最多遊戲玩家使用的通訊軟體


### 語法參考

Markdown 基本語法:  
<https://www.markdownguide.org/basic-syntax/>


## Kramdown

### 簡介

Kramdown語法是Markdown語法的超集  
前面的 kram 其實就是把 mark 倒過來寫

kramdown是預設的Jekyll Markdown處理器。  
使用 Jekyll 建立網站時，
您可以使用標準的 Markdown 語法和一些特定的 kramdown 語法。  
Jekyll 會將你的 Markdown/kramdown 渲染成 HTML。

*[HTML]: 超文本標記語言（英語：HyperText Markup Language，簡稱：HTML）

### 語法參考

Kramdown基本語法參考:  
<https://kramdown.gettalong.org/quickref.html>  
<https://gohom.win/2015/11/06/Kramdown-note/>
<https://yufree.cn/2014/10/25/kramdown>
<https://zhuanlan.zhihu.com/p/60838339>

[full list of syntax highlighting support language][codeblock-language]

[codeblock-language]: https://www.fabriziomusacchio.com/blog/2021-08-11-Syntax_Highlighting_in_Jekyll/ codeblock支援語法高亮的(程式)語言

## HTML vs Markdown vs Kramdown

這裡僅列出部分基本語法與HTML的差異

| 英文           | 中文    | HTML                                 | Markdown   | Kramdown |
| -------------- |:----    | ------------------------------------:|:----------:|:--------:|
| bold           | 粗體    | <b>粗體<b>                           | **粗體**   | 同左     |
| italic         | 斜體    | <i>斜體</i>                          | __斜體__   | 同左     |
| strikethrought | 刪除線  | <s>刪除線</s>                        | ~~刪除線~~ | 同左     |
| underline      | 底線    | <u>底線</u>                          | 不支援     | 先用HTML |
| color          | 顏色    | <span style="color: red">紅字</span> | 不支援     | 先用HTML |

> [!WARNNING]  
> 其他不常用的或不支援的就直接用 HTML

> [!ALERT]  
> Kramdown有他的簡化寫法,但是我還沒研究


## 其他: 關於 blockquote 裡面的 alert

通常 markdown 文檔可以支援
- `[!NOTE]`
- `[!WARNNING]`
- `[!ALERT]`
會有對應圖案

如果這樣寫:
~~~markdown
> [!NOTE]
> Highlights information that users should take into account, even when skimming.

> [!IMPORTANT]
> Crucial information necessary for users to succeed.

> [!WARNING]
> Critical content demanding immediate user attention due to potential risks.
~~~

會變成這樣:
![圖片](https://docs.github.com/assets/cb-41128/mw-1440/images/help/writing/alerts-rendered.webp)

請參考: [github 的 blockquote 裡面的 alert](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#alerts)

不過這點在 jekyll 上不支援就是了
但我習慣還是會這樣寫

--------------------------------------------------

# 以下是上面文章的原始文件:

~~~~~~md
目錄 TOC (Table Of Contene)

* 此行是必需的，但不會出現。將 '*' 替換為 '1' 以建立編號清單。
{:toc}

# Markdown/Kramdown 是什麼？

![markdown](/assets/markdown.png){:height="48px" width="36px"}

## Markdown

### 簡介

![markdown](/assets/markdown.png)
> markdown不能加圖片說明文字,可以自己打在下一行

Markdown 是一種 **[輕量級標記語言][輕量級標記語言定義]**，
可用於為__純文字文件新增格式元素__。

Markdown 由 **[John Gruber][John Gruber資訊]** 於 2004 年創建，
現已成為世界上最受歡迎的標記語言之一。


[輕量級標記語言定義]: https://zh.wikipedia.org/zh-tw/輕量級標記語言 （英語：Lightweight Markup Language，簡稱LML）是一類用簡單句法描述簡單格式的文本語言。
[John Gruber資訊]: https://daringfireball.net/projects/markdown/

### 特性

根據 [維基百科][markdown維基百科]

[markdown維基百科]: https://zh.wikipedia.org/zh-tw/Markdown

由於Markdown:
1. 輕量化
2. 易讀
3. 易寫
4. 並且支援:
  + 圖片
  * 圖表
  - Latex數學公式
    - 似乎有些瀏覽器不支援顯示 Latex,  
      ~~比如說手機版的 Google Chrome~~

目前許多網站都廣泛使用Markdown:
- 撰寫說明文件,  
  比如說 Github
- 用於論壇上發表訊息  
  比如說 Discord

*[Github] 最多人使用的 git 版本管理倉庫遠端託管平臺

*[Discord] 最多遊戲玩家使用的通訊軟體

### 語法參考

Markdown 基本語法:  
<https://www.markdownguide.org/basic-syntax/>


## Kramdown

### 簡介

Kramdown語法是Markdown語法的超集  
前面的 kram 其實就是把 mark 倒過來寫

kramdown是預設的Jekyll Markdown處理器。  
使用 Jekyll 建立網站時，
您可以使用標準的 Markdown 語法和一些特定的 kramdown 語法。  
Jekyll 會將你的 Markdown/kramdown 渲染成 HTML。

*[HTML]: 超文本標記語言（英語：HyperText Markup Language，簡稱：HTML）

### 語法參考

Kramdown基本語法參考:  
<https://kramdown.gettalong.org/quickref.html>  
<https://gohom.win/2015/11/06/Kramdown-note/>
<https://yufree.cn/2014/10/25/kramdown>
<https://zhuanlan.zhihu.com/p/60838339>

## HTML vs Markdown vs Kramdown

這裡僅列出部分基本語法與HTML的差異

> 不支援的就直接用 HTML

| 英文           | 中文    | HTML                                 | Markdown   | Kramdown |
| -------------- |:----    | ------------------------------------:|:----------:|:--------:|
| bold           | 粗體    | <b>粗體<b>                           | **粗體**   | 同左     |
| italic         | 斜體    | <i>斜體</i>                          | __斜體__   | 同左     |
| strikethrought | 刪除線  | <s>刪除線</s>                        | ~~刪除線~~ | 同左     |
| underline      | 底線    | <u>底線</u>                          | 不支援     | 先用HTML |
| color          | 顏色    | <span style="color: red">紅字</span> | 不支援     | 先用HTML |

> [!WARNNING]
> 其他不常用的或不支援的就直接用 HTML

> [!ALERT]
> Kramdown有他的簡化寫法,但是我還沒研究

## 其他: 關於 blockquote 裡面的 alert

通常 markdown 文檔可以支援
- `[!NOTE]`
- `[!WARNNING]`
- `[!ALERT]`
會有對應圖案

如果這樣寫:
```markdown
> [!NOTE]
> Highlights information that users should take into account, even when skimming.

> [!IMPORTANT]
> Crucial information necessary for users to succeed.

> [!WARNING]
> Critical content demanding immediate user attention due to potential risks.
```

會變成這樣:
![圖片](https://docs.github.com/assets/cb-41128/mw-1440/images/help/writing/alerts-rendered.webp)

請參考: [github 的 blockquote 裡面的 alert](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#alerts)

不過這點在 jekyll 上不支援就是了
但我習慣還是會這樣寫

~~~~~~~

--------------------------------------------------

後面是一些簡單說明, 有興趣再看

--------------------------------------------------

## block 級元素


## span 列級元素
### markdown 原生支援
- **粗體 bold**
- italic_` _斜體 italic_  
- ~~刪除線 strikethrought~~
### markdown 不支援, 但還是可以用 HTML 語法:
- <u>底線</u>
- <tt>細字</tt>
- <sup>上標字型</sup>
- <sub>下標字型</sub>

> markdown語法支援 emoji: ��⭐️�，  
> 不過在編輯時要看你的字型是否支援。--
> 在 Window10 以上的版本,可以按 Win + ; 叫出 emoji 選單






--------------------------------------------------

## 這些功能 markdown 沒有, 還是可以用 html 語法處理:

```html
<u>底線</u> <tt>細字</tt> <sup>上標字型</sup> <sub>下標字型</sub>
```
結果:

<u>底線</u> <tt>細字</tt> <sup>上標字型</sup> <sub>下標字型</sub>

--------------------------------------------------

## 顏色

```markdown
要使用 html 元素才能上顏色:  
這個字是<span style="color: red">紅色</span>的

建議使用 span inline attribute list (span IAL)  
這個字是*綠色*{: style="color: green"}的
```

要使用 html 元素才能上顏色:  
這個字是<span style="color: red">紅色</span>的

建議使用 span inline attribute list (span IAL)  
這個字是*綠色*{: style="color: green"}的


--------------------------------------------------

## comment 隱藏註解

~~~markdown
這是一個段落
{::comment}
這是我們自己看的隱藏註解  
不會顯示在網頁上  
不過如果使用 公開的 github 倉庫發表網頁  
還是可以去 github 倉庫查看
{:/comment}
段落繼續...
~~~

這是一個段落
{::comment}
這是我們自己看的隱藏註解  
不會顯示在網頁上  
不過如果使用 公開的 github 倉庫發表網頁  
還是可以去 github 倉庫查看
{:/comment}
段落繼續...

--------------------------------------------------

## 超連結(Hyperlink) or 檔案:

```markdown
這是一個網址:
<https://zh.wikipedia.org/zh-tw/Markdown>

這行有一個超連結: [這是Markdown 維基百科的網址](https://zh.wikipedia.org/zh-tw/Markdown)

把滑鼠移到這個超連結上面，會顯示標提: [連結](https://zh.wikipedia.org/zh-tw/Markdown "Markdown維基百科")

超連結推薦這樣寫,對於編輯與閱讀比較簡潔: [link][markdown wiki]

[markdown wiki]: https://zh.wikipedia.org/zh-tw/Markdown
```

這是一個網址:
<https://zh.wikipedia.org/zh-tw/Markdown>

這行有一個超連結: [這是Markdown 維基百科的網址](https://zh.wikipedia.org/zh-tw/Markdown)

把滑鼠移到這個超連結上面，會顯示標提: [連結](https://zh.wikipedia.org/zh-tw/Markdown "Markdown維基百科")

超連結推薦這樣寫,對於編輯與閱讀比較簡潔: [link][markdown wiki]

[markdown wiki]: https://zh.wikipedia.org/zh-tw/Markdown

--------------------------------------------------

## 圖片跟超連結很像,但是前面加一個驚歎號

```markdown
![這是圖片名稱](/assets/markdown.png)
markdown不能加圖片說明文字,可以自己打在下一行
```

![這是圖片名稱](/assets/markdown.png)
markdown不能加圖片說明文字,可以自己打在下一行

----------------------------------------------
## Paragraphs 段落

~~~ markdown
連續的文字視為段落,
這句話在同一個段落,
同一個段落的文字,
可以在後面加上兩個空格  
或是兩個反斜線\\
來換行

可以空一行切到下一個段落
~~~

連續的文字視為段落,
這句話在同一個段落,
同一個段落的文字,
可以在後面加上兩個空格  
或是兩個反斜線\\
來換行

可以空一行切到下一個段落

----------------------------------------------

## Headers 標頭



~~~ markdown
目錄 TOC (Table Of Contene)

* 此行是必需的，但不會出現。將 '*' 替換為 '1' 以建立編號清單。
{:toc}

前面兩種寫法的=或-數量只要有一個就行  
不過寫多一點看比較清楚

First level header 一級標頭
===================

Second level header 二級標頭
-------------------

# H1 header 一級標頭 {#ID1}
## H2 header 二級標頭
### H3 header 三級標頭 {#ID2}
#### H4 header 四級標頭
##### H5 header 五級標頭
###### H6 header 六級標頭
{:.no_toc}
後面加了{:.no_toc}就不會顯示在toc目錄上面
~~~


* 此行是必需的，但不會出現。將 '*' 替換為 '1' 以建立編號清單。
{:toc}


First level header 一級標頭
===

Second level header 二級標頭
-------------------

# H1 header 一級標頭,後面我加了ID {#ID1}
## H2 header 二級標頭
### H3 header 三級標頭,後面我加了ID  {#ID2}
#### H4 header 四級標頭
##### H5 header 五級標頭
###### H6 header 六級標頭
{:.no_toc}

[點這裡可以跳到加了ID的一級標頭](#ID1)

[點這裡可以跳到加了ID的三級標頭](#ID2)

> 跳到加ID標頭時,  
> 要往上一點點才會看到標頭,  
> 基本上是跳過去看內容的

**********************************************

## Blockquotes 區塊引用

~~~ markdown
> 範例 區塊引用.
>
> > 多層 區塊引用,
> > 也可以
>
> ## 也可以在裡面加上標頭 Headers
> This is the outer quote again.

> [!alert] 這是另一個 區塊引用,
只要沒空行,
就一樣在 區塊引用 裡面

空一行就變成另一個段落
~~~

> 範例 區塊引用.
>
> > 多層 區塊引用s,
> > 也可以
>
> ## 也可以在裡面加上標頭 Headers
> This is the outer quote again.

> [!alert] 這是另一個 區塊引用,
只要沒空行,
就一樣在 區塊引用 裡面

空一行就變成另一個段落

-------------------------------------------

## Code block 程式碼區塊

大致上支援的語言可以在這裡查看:  
<https://www.fabriziomusacchio.com/blog/2021-08-11-Syntax_Highlighting_in_Jekyll/>  
<https://simpleit.rocks/ruby/jekyll/what-are-the-supported-language-highlighters-in-jekyll/>
<https://michaelcurrin.github.io/dev-cheatsheets/cheatsheets/jekyll/code-blocks/supported-languages.html>
<https://haisum.github.io/2014/11/07/jekyll-pygments-supported-highlighters/>

~~~ markdownk
第一種, 比較少見  
斷行之後, 前面加上 4 個空格, 或是 1 個 Tab

    四個空格的程式碼區塊從這裡開始
~~~

第二種, 比較常見  
在程式碼區塊前後斷行使用 ~ 或 ` ,  
後面的符號數量要>=前面的
```markdown
~~~markdown
> 這裡是程式碼區塊內容
> 可以寫一些程式碼
> # 比如說 markdown 語法
~~~
~~~python
# 或是 python 程式碼
import pandas as pd
df = pd.read_csv(".data.csv")
print(df)
~~~
```

單行程式碼區塊, 或是要把該行某幾個字框起來變成程式碼區塊
可以在前後加上 ` 符號

`長的單行程式碼區塊不應換行。如果它們太長，它們應該水平滾動。這條線應該可以證明他真的很長。`


不過不是所有語言都能支援,
比如說 mql5 就沒有支援:

```mql5
void OnStart()
{
  printf("123");
}
```
 
----------------------------------------------

## Horizontal Rules 水平分格線

在空白行上使用三個或更多星號、破折號或下劃線，
可以選擇用空格或Tab分隔
前後要空行,以免後面加了---變成二級標頭

```markdown

***

---

> 在 codeblock裡面,使用底線_連在一起的情況,  
> 必須兩個一組,不然看起來粗細不同
_____

___


 * * * *
   _ _ _ _ _

-----------
```

分隔線看起來就像這樣:

 * * * *
   _ _ _ _ _

-----------


----------------------------------------------

## List 列表

Kramdown 支援有序和無序列表。
有序清單的開頭是一個數位，後跟一個句點、一個空格，然後是清單項文本。
清單項的內容由塊級元素組成。
與帶有清單標記的行的文字具有相同縮進的所有行都屬於清單項：

~~~ markdown
1. 列表項目1
2. 另一個列表項目
3. 第三個列表項目,  
   有兩行,後面記得加兩個空格段行
4. 第四個列表項目,

   > 裡面有 blockquote

   ###### 還有 Header

5. 第五個列表項目
   裡面還有一層無序列表, 交換順序沒差
   - 列表 5.1. 前面用 - 號
   + 列表 5.2. 前面用 + 號
   * 列表 5.3. 前面用 * 號

6. 第六個列表項目
   裡面還有一層有序列表,交換順序要記得自己改編號
   1. 列表6.1.
   2. 列表6.2.
      + 列表6.2.1
      * 列表6.2.2

這是另一個無序列表,我們可以觀察不同層級的項目符號長得不一樣
- 項目1
  - 項目2
    - 項目3
      - 項目4 跟 項目3 的符號相同


這是一個有待辦事項的清單列表:  
完成打x, 未完成空白

- [x] 這是一個完成的事項
- [ ] 這是一個完成的事項
~~~

1. 列表項目1
2. 另一個列表項目
3. 第三個列表項目,  
   有兩行,後面記得加兩個空格段行
4. 第四個列表項目,

   > 列表裡面可以放 blockquote

   ###### 列表裡面也可以放 Header

5. 第五個列表項目
   裡面還有一層無序列表, 交換順序沒差
   - 列表 5.1. 前面用 - 號
   + 列表 5.2. 前面用 + 號
   * 列表 5.3. 前面用 * 號

6. 第六個列表項目
   裡面還有一層有序列表,交換順序要記得自己改編號
   1. 列表6.1.
   2. 列表6.2.
      + 列表6.2.1
      * 列表6.2.2

這是另一個無序列表,我們可以觀察不同層級的項目符號長得不一樣
- 項目1
  - 項目2
    - 項目3
      - 項目4 跟 項目3 的符號相同

這是一個有待辦事項的清單列表:  
完成打x, 未完成空白

- [x] 這是一個完成的事項
- [ ] 這是一個完成的事項

--------------------------------------------------------

## Abbreviations 縮寫

~~~markdown
這句話的 ASDF 有縮寫的提示,  
縮寫定義可以寫在任何地方, 本頁面的關鍵字都會有提示

*[ASDF]: 這是 ASDF 的定義, 定義只能在同一行
~~~

這句話的 ASDF 有縮寫的提示,  
縮寫定義可以寫在任何地方, 本頁面的關鍵字都會有提示

*[ASDF]: 這是 ASDF 的定義, 定義只能在同一行

-------------------------------------------------------

## footnote 註腳,腳註,腳注,引用,註解,定義

腳註雖然寫在這裡, 不過實際會顯示在頁面最下面

~~~markdown
這是一個簡單的腳註，[^1]，這是一個比較長的腳註。[^bignote]

[^1]：這是第一個腳註。

[^bignote]：這裡有多個段落和程式碼。

    縮排段落以將其包含在腳註中。

    `{我的程式碼}`

    添加任意數量的段落。
~~~

這是一個簡單的腳註，[^1]，這是一個比較長的腳註。[^bignote]

[^1]：這是第一個腳註。

[^bignote]：這裡有多個段落和程式碼。

    縮排段落以將其包含在腳註中。

    `{我的程式碼}`

    添加任意數量的段落。

-------------------------------------------------------

## 表格

markdown 支援表格

~~~markdown
這是一個表格,前後要空行

| Header1 | Header2 | Header3 | 靠左 | 置中 | 靠右 |
|:--------|:-------:|--------:|:-----|:----:|-----:|
| cell1   | cell2   | cell3   | 1    | 1    | 1    |
| cell4   | cell5   | cell6   | 2    | 2    | 2    |
|----
| cell1   | cell2   | cell3   | 3    | 3    | 3    |
| cell4   | cell5   | cell6   | 4    | 4    | 4    |
|=====
| Foot1   | Foot2   | Foot3   | 5    | 5    | 5    |
{: rules="groups"}

Foot:
- 字比較大
- 通常用於 加總或是總結

另一個範例:

| Name | Age | Score |
|------|-----|-------|
| Alice | 20 | 90 |
| Bob | 21 | 85 |
| Charlie | 19 | 95 |
| Average | = | 90 |
~~~

在codeblock裡面,
線看起來沒有對齊的問題,
要去調成等寬字型(mono font)  
不過很遺憾的是 google fonts 上面沒有任何繁體中文的等寬字型

這是一個表格,前後要空行

| Header1 | Header2 | Header3 | 靠左 | 置中 | 靠右 |
|:--------|:-------:|--------:|:-----|:----:|-----:|
| cell1   | cell2   | cell3   | 1    | 1    | 1    |
| cell4   | cell5   | cell6   | 2    | 2    | 2    |
|----
| cell1   | cell2   | cell3   | 3    | 3    | 3    |
| cell4   | cell5   | cell6   | 4    | 4    | 4    |
|=====
| Foot1   | Foot2   | Foot3   | 5    | 5    | 5    |
{: rules="groups"}

Foot:
- 字比較大
- 通常用於 加總或是總結

另一個範例:

| Name | Age | Score |
|------|-----|-------|
| Alice | 20 | 90 |
| Bob | 21 | 85 |
| Charlie | 19 | 95 |
| Average | = | 90 |


----------------------------------------------------

## Definition List 定義列表

~~~markdown
定義名
: 定義1
: 定義2,
這行也是定義2

另一個定義名
: 定義1,
  這行也是定義1
: 定義2

: 定義3,
空了1行,  
  就算後面加了斷行符號,\\
  還是在同一個定義名裡面?


這行不是定義
~~~

定義名
: 定義1
: 定義2,
這行也是定義2

另一個定義名
: 定義1,
  這行也是定義1
: 定義2

: 定義3,
空了1行,  
  就算後面加了斷行符號,\\
  還是在同一個定義名裡面?

這行不是定義

  這行前面有兩個空格


----------------------------------------------------
