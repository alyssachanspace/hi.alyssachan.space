# 0成本0基礎DIY網路名片



## 目錄
1. [HTML教學](#html)
   1. [基本 HTML5 結構](#html5)
   2. [常見 HTML 語義化元素](#html_semantic)
2. [CSS教學](#css)
   1. [CSS 選擇器](#css_selector)
   2. [常用 CSS 屬性](#css_property)
   3. [響應式設計](#rwd)
3. [網路名片模板](#template)

## <a name="html"></a>HTML教學
[HTML](https://developer.mozilla.org/zh-CN/docs/Glossary/HTML#select-language)（HyperText Markup Language 超文本標記語言） 是一種描述語言，用來定義網頁結構。

HTML 文檔是包含多個 **HTML 元素** 的文本文檔。每個元素都用一對開始和結束 **標籤** 包裹。每個標籤以尖括號（ `<>` ）開始和結束。也有一部分標籤中不需要包含文本，這些標籤稱為空標籤，如 `<br>` 、 `<hr>` 和 `<img>` 。

你可以使用 **屬性** 來擴展 HTML 標籤。

`<p class="greeting">Hello</p>`

- `<p>` 是標籤
- `class` 是屬性， `greeting` 是屬性值
- `Hello` 是文本內容

### <a name="html5"></a>基本 HTML5 結構
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  ...
</body>
</html>
```
- [`<!DOCTYPE>`](https://developer.mozilla.org/en-US/docs/Glossary/Doctype) 是文件類型宣告，告知瀏覽器這個文件是用哪個版本的 HTML（或 XML）撰寫。`<!DOCTYPE html>` 代表 HTML5。
- `<html> ... </html>` 中的文字描述了一個 HTML 文件
- `<head> ... </head>` 中的文字提供了文件資訊
- `<body> ... </body>` 中的文字描述了網頁中顯示的內容
- [`lang`](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/lang) 表示網頁的語言，可以加上地區指定地方方言，例如：
  - `lang="en"` 英文
  - `lang="en-US"` 美式英文
  - `lang="en-GB"` 英式英文
  - `lang="zh"` 中文
  - `lang="zh-Hans"` 簡體中文
  - `lang="zh-CN"` 中國簡體中文
  - `lang="zh-Hant"` 繁體中文
  - `lang="zh-TW"` 台灣繁體中文
  - `lang="zh-HK"` 香港繁體中文
- [`<meta>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta) 表示中繼資料
  - `charset` 代表字符編碼，一般使用 `utf-8`
  - `content` 包含 `http-equiv` 或 `name` 屬性的值
  - `http-equiv` 定義編譯指示指令，通常用來設定IE兼容模式
    - `<meta http-equiv="X-UA-Compatible" content="IE=edge">` 代表標準模式
  - `viewport` 指網頁在瀏覽器上的可視範圍，與響應式網頁設計（Responsive Web Design, RWD）息息相關
    - `<meta name="viewport" content="width=device-width, initial-scale=1.0">` 指定螢幕寬度為裝置寬度，畫面載入初始縮放比例 100%
- `<title>` 表示文件標題

### <a name="html_semantic"></a>常見 HTML 語義化元素
| 元素 | 說明 | 格式 |
| --- | --- | --- |
| [`<header>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/header) | 頁首 | `<header>...</header>` |
| [`<nav>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nav) | 導覽 | `<nav>...</nav>` |
| [`<main>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main) | 主體部分 | `<main>...</main>` |
| [`<section>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/section) | 獨立的部分 | `<section>...</section>` |
| [`<article>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/article) | 可重複使用的獨立結構 | `<article>...</article>` |
| [`<figure>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/figure) | 附加內容，如圖片、表格 | `<figure><img src="圖片網址" alt="替代文字" /><figcaption>說明</figcaption></figure>` |
| [`<figcaption>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/figcaption) | 說明/標題 | `<figure><img src="圖片網址" alt="替代文字" /><figcaption>說明</figcaption></figure>` |
| [`<aside>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/aside) | 側欄 | `<aside>...</aside>` |
| [`<footer>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/footer) | 頁尾 | `<footer>...</footer>` |

### <a name="html_element"></a>常見 HTML 元素
| 元素 | 說明 | 格式 |
| --- | --- | --- |
| [`<h1> - <h6>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements)      | 標題1 - 標題6 | `<h1>大標題</h1>` |
| [`<p>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/p) | 段落 | `<p>我是段落</p>` |
| [`<br>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/br) | 斷行 | `第一行文字<br />第二行文字` |
| [`<span>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/span) | 短語 | `<span>我是短語</span>` |
| [`<strong>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/strong) | 粗體 | `<strong>粗體文字</strong>` |
| [`<em>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/em) | 強調（常以斜體表示） | `<em>強調文字</em>` |
| [`<a>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a) | 連結 | `<a href="連結">顯示文字</a>` |
| [`<small>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/small) | 把字體變小一號 | `<small>我是小字</small>` |
| [`<img>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img) | 圖片 | `<img src="圖片網址" alt="替代文字" />` |
| [`<div>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/div) | 區塊容器 | `<div>內容</div>` |
| [`<hr>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/hr) | 分隔線 | `<hr />` |
| [`<ul>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul) | 項目符號列表 | `<ul><li>項目</li><li>項目</li></ul>` |
| [`<ol>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol) | 編號列表 | `<ol><li>第一點</li><li>第二點</li></ol>` |
| [`<table>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table) | 表格 |  `<table><thead><tr><th>標題</th></tr></thead><tbody><tr><td>儲存格</td></tr></tbody></table>` |
| [`<blockquote>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote) | 引文 | `<blockquote cite="來源網址"><p>引文</p></blockquote>` |

## <a name="css"></a>CSS教學
[CSS](https://developer.mozilla.org/en-US/docs/Glossary/CSS) （Cascading Style Sheets 層疊樣式表）是用來控制網頁在瀏覽器中的顯示外觀的聲明式語言。瀏覽器會根據 CSS 的樣式來顯示元素。一條 CSS 的樣式定義包括屬性和屬性值，它們共同決定網頁的外觀。

```
p {
  background: #f2f2f2;
}
```
- `p` 是元素
- `background` 是屬性， `#f2f2f2` 是屬性㥀

有3種方式加入CSS：
1. Inline CSS，在標籤中定義 `style`，例：`<p style="background: #f2f2f2;">段落</p>`
2. Internal CSS，在 `<head>` 中定義 `<style>`，例：`<style>p { background: #f2f2f2; }</style>`
3. External CSS，在 `<head>` 中連結外部樣式表，例：`<link rel="stylesheet" href="https://necolas.github.io/normalize.css/8.0.1/normalize.css">`

### <a name="css_selector"></a>CSS 選擇器
| CSS 選擇器 | 例子 |
| --- | --- |
| [通配](https://developer.mozilla.org/en-US/docs/Web/CSS/Universal_selectors) | `* { ... }` 選擇所有HTML元素 |
| [類型](https://developer.mozilla.org/en-US/docs/Web/CSS/Type_selectors) | `p { ... }` 選擇所有 `<p>` 元素 |
| [類名](https://developer.mozilla.org/en-US/docs/Web/CSS/Class_selectors) | `p.title { ... }` 選擇所有 `<p class="title">` 的元素 |
| [ID](https://developer.mozilla.org/en-US/docs/Web/CSS/ID_selectors) | `p#one { ... }` 選擇 `<p id="one">` 的那一個元素 |
| [後代](https://developer.mozilla.org/en-US/docs/Web/CSS/Descendant_combinator) | `p span { ... }` 選擇所有在 `<p>` 元素中的 `<span>` 元素 |
| [子代](https://developer.mozilla.org/en-US/docs/Web/CSS/Child_combinator) | `div > h2 { ... }` 選擇所有直接在 `<div>` 元素之下的 `<h2>` 元素 |
| [通用兄弟](https://developer.mozilla.org/en-US/docs/Web/CSS/General_sibling_combinator) | `h2 ~ p { ... }` 選擇所有和 `<h2>` 元素同層級的 `<p>` 元素 |
| [相鄰兄弟](https://developer.mozilla.org/en-US/docs/Web/CSS/Adjacent_sibling_combinator) | `h2 + p { ... }` 選擇所有緊接著 `<h2>` 元素之後的 `<p>` 元素 |
| [屬性](https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors) | <ul><li>`a[target="_blank"] { ... }` 選擇所有 `<a target="_blank">` 的元素</li><li>`a[href^="#"] { ... }` 選擇所有 `<a href="#...">` （開頭）的元素</li><li>`[lang\|="en"] { ... }` 選擇所有 `lang="en..."` （屬性值開頭）的元素</li><li>`a[href$=".pdf"] { ... }` 選擇所有 `<a href="...pdf">` （結尾）的元素</li><li>`a[title~="word"] { ... }` 選擇所有 `<a title="... word ...">` （含有完整字眼）的元素</li><li>`a[title*="substring"] { ... }` 選擇所有 `<a title="...substring...">` （含有字眼）的元素</ul> |
| [反選](https://developer.mozilla.org/en-US/docs/Web/CSS/:not) | `:not(p) { ... }` 選擇所有不是 `<p>` 的元素 |
| 連結 | <ul><li>[`:link { ... }`](https://developer.mozilla.org/en-US/docs/Web/CSS/:link) 選擇所有未探訪過的連結</li><li>[`:visited { ... }`](https://developer.mozilla.org/en-US/docs/Web/CSS/:visited) 選擇所有已探訪過的連結</li><li>[`:hover { ... }`](https://developer.mozilla.org/en-US/docs/Web/CSS/:hover) 鼠標停留時的顯示</li><li>[`:active { ... }`](https://developer.mozilla.org/en-US/docs/Web/CSS/:active) 正在點選的連結</li></ul> |
| 次序 | <ul><li>`:first-child { ... }` 選擇第一個元素</li><li>`:last-child { ... }` 選擇最後一個元素</li><li>`:nth-child(even) { ... }` 選擇排在雙數的元素，即第2, 4, 6, ... 個</li><li>`:nth-child(odd) { ... }` 選擇排在單數的元素，即第1, 3, 5, ... 個</li><li>`:nth-child(3n+1) { ... }` 選擇排在 `3n+1` 的元素，即第1, 4, 7, ... 個</li></ul> |

### <a name="css_property"></a>常用 CSS 屬性
| CSS 屬性 | 說明 | 值 |
| --- | --- | --- |
| [`background`](https://developer.mozilla.org/en-US/docs/Web/CSS/background) | 背景 | 屬性有<ul><li> [`background-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color) 背景色</li><li>[`background-position`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-position) 背景位置</li><li>[`background-repeat`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-repeat) 背景重複</li><li>[`background-size`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-size) 背景尺寸：`cover` 完全覆蓋（可能被裁）、 `contain` 全幅（可能有空白）、長度或百分比</li><li>[`background-image`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-image) 背景圖</li><li>[`background-origin`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-origin) 背景圖相對區域</li><li>[`background-attachment`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-attachment) 背景固定或滾動</li><li>[`background-clip`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-clip) 背景延伸</li></ul>例：`center / contain no-repeat url("圖片網址")` 置中 全幅 不重複 背景圖 |
| [`color`](https://developer.mozilla.org/en-US/docs/Web/CSS/color) | 前景色 | 顏色如 `#000` |
| [`font-family`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family) | 字體順序 | 以逗號 (,) 分隔字體，前面優先使用，如`Georgia, serif` |
| [`font-size`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size) | 字體大小 | 長度如 `1rem` |
| [`font-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-style) | 字體傾斜 | `italic` |
| [`font-weight`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight) | 字體粗度 | `bold` |
| [`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align) | 文字對齊 | <p style="text-align:left">`left` 靠左對齊</p><p style="text-align:center">`center` 置中對齊</p><p style="text-align:right">`right` 靠右對齊</p><p style="text-align:justify">`justify` 左右對齊，不包最後一行</p><p style="text-align:justify-all">`justify-all` 左右對齊，包括最後一行</p> |
| [`text-decoration`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration) | 文字裝飾 | `underline` <span style="text-decoration:underline">底線</span><br>`underline wavy` <span style="text-decoration:underline wavy">波浪底線</span><br>`underline dashed` <span style="text-decoration:underline dashed">虛底線</span><br>`overline` <span style="text-decoration:overline">頂線</span><br>`overline underline` <span style="text-decoration:overline underline">頂低線</span><br>`line-through` <span style="text-decoration:line-through">刪除線</span> |
| [`letter-spacing`](https://developer.mozilla.org/en-US/docs/Web/CSS/letter-spacing) | 文字間距 | 長度如 `1px` |
| [`line-height`](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height) | 行距 | 數字如 `1.75` |
| [`text-shadow`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-shadow) | 文字陰影 | <p>屬性 `offset-x offset-y blur-radius color`，例</p><div style="background:#fff;padding:5px"><span style="text-shadow: 1px 1px 10px rgba(0,0,0,0.5)">`text-shadow: 1px 1px 10px rgba(0,0,0,0.5)`</span></div> |
| [`box-shadow`](https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow) | 區塊陰影 | <p>屬性 `offset-x offset-y blur-radius color`，例</p><div style="box-shadow: 1px 1px 10px rgba(0,0,0,0.5);background:#fff;padding:5px">`box-shadow: 1px 1px 10px rgba(0,0,0,0.5)`</div> |
| [`width`](https://developer.mozilla.org/en-US/docs/Web/CSS/width) | 寬度 | 長度如 `600px` |
| [`max-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/max-width) | 最大寬度 | 長度如 `100%` |
| [`height`](https://developer.mozilla.org/en-US/docs/Web/CSS/height) | 高度 | 長度如 `100px` |
| [`display`](https://developer.mozilla.org/en-US/docs/Web/CSS/display) | 顯示佈局 | `inline` 行文佈局<br>`block` 區塊佈局<br>`flex` 彈性佈局<br>`grid` 網格佈局 |
| [`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin) | 外邊距 | 是 `margin-top margin-right margin-bottom margin-left` 的簡寫，以長度為值，例<ul><li>`10px`：四邊`10px`</li><li>`10px auto`：上下`10px`，左右自動（置中）</li><li>`10px auto 20px`：上邊`10px`，左右自動，下邊`20px`</li><li>`10px 20px 0 30px`：上邊`10px`，右邊`20px`，下邊`0`，左邊`30px`</li></ul> |
| [`padding`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding) | 內邊距 | 是 `padding-top padding-right padding-bottom padding-left` 的簡寫，用法跟`margin`一樣，以長度為值 |
| [`border`](https://developer.mozilla.org/en-US/docs/Web/CSS/border) |  邊框 | <p>是 `border-top border-right border-bottom border-left` 的簡寫，屬性有 `border-width border-style border-color`，例<br>`border-bottom: 1px dotted #ff0000;` <span style="border-bottom: 3px solid #ff0000;">紅色3px底線</span></p><p>`border-style`：</p><ul style="line-height:40px"><li><span style="inline-block; background: #f2f2f2; padding: 5px; margin: 20px 10px 20px 0; border:none">`none` 無</span></li><li><span style="inline-block; background: #f2f2f2; padding: 5px; margin: 20px 10px 20px 0; border:hidden">`hidden` 隱藏</span></li><li><span style="inline-block; background: #f2f2f2; padding: 5px; margin: 20px 10px 20px 0; border:3px dotted #ff0000">`dotted` 圓點</span></li><li><span style="inline-block; background: #f2f2f2; padding: 5px; margin: 20px 10px 20px 0; border:3px dashed #ff0000">`dashed` 虛線</span></li><li><span style="inline-block; background: #f2f2f2; padding: 5px; margin: 20px 10px 20px 0; border:3px solid #ff0000">`solid` 實線</span></li><li><span style="inline-block; background: #f2f2f2; padding: 5px; margin: 20px 10px 20px 0; border:3px double #ff0000">`double` 雙實線</span></li><li><span style="inline-block; background: #f2f2f2; padding: 5px; margin: 20px 10px 20px 0; border:3px groove #ff0000">`groove` 雕刻效果</span></li><li><span style="inline-block; background: #f2f2f2; padding: 5px; margin: 20px 10px 20px 0; border:3px ridge #ff0000">`ridge` 浮雕效果</span></li><li><span style="inline-block; background: #f2f2f2; padding: 5px; margin: 20px 10px 20px 0; border:3px inset #ff0000">`inset` 陷入效果</span></li><li><span style="inline-block; background: #f2f2f2; padding: 5px; margin: 20px 10px 20px 0; border:3px outset #ff0000">`outset` 突出效果</li></ul> |
| [`border-radius`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius) | 邊框圖角 | <p>長度如 <span style="inline-block; background: #f2f2f2; padding: 10px; margin: 20px 10px 20px 0; border-radius:3px">`3px`</span>、<span style="inline-block; background: #f2f2f2; padding: 10px; margin: 20px 10px 20px 0; border-radius:50%">`50%`</span></p> |
| [`box-sizing`](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing) | 區塊尺寸 | `content-box` 預設值，以內容範圍計算總寬度及高度<br>`border-box` 以邊框範圍計算總寬度及高度 |
| [`position`](https://developer.mozilla.org/en-US/docs/Web/CSS/position) | 定位 | <ul><li>`static` 正常佈局</li><li>`relative` 相對定位</li><li>`absolute` 絕對定位，以上一個相對定位為原點</li><li>`fixed` 固定定位，以視窗為原點</li><li>`sticky` 粘性定位</li></ul> |
| [`object-fit`](https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit) | 指定可替換元素在元素框內的對齊方式 | <ul><li>`fill` 預設值，完全填充</li><li>`contain` 全幅</li><li>`cover` 完全覆蓋</li><li>`none` 保持原尺寸</li><li>`scale-down` 取 `none` 或 `contain` 之間更小的一個</li></ul> |
| [`opacity`](https://developer.mozilla.org/en-US/docs/Web/CSS/opacity) | 不透明度 | `0` 到 `1` 之間的數字<ul><li>`1.0` 預設值，完全不透明</li><li>`0` 是完全透明</li></ul> |
| [`overflow`](https://developer.mozilla.org/en-US/docs/Web/CSS/overflow) | 溢出顯示 | <ul><li>`visible` 預設值，內容不會被修剪，可以呈現在元素框之外</li><li>`hidden` 內容將被剪裁以適合填充框，無滾動條</li><li>`scroll` 內容將被剪裁以適合填充框，顯示滾動條</li><li>`auto` 取決於瀏覽器，如內容溢出，桌面瀏覽器會提供滾動條</li></ul> |

### <a name="rwd"></a>響應式設計
[Media Queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries) 幫助我們根據設備的大致類型（如打印設備與帶屏幕的設備）或者特定的特徵和設備參數（例如屏幕分辨率和瀏覽器視窗寬度）來修改網站或應用程序時。
#### [`@media`](https://developer.mozilla.org/en-US/docs/Web/CSS/@media) 用法
`@media screen and (min-width: 1200px) { ... }` 瀏覽器視窗寬度最少 `1200px` 以上

## <a name="template"></a>網路名片模板
到 https://codepen.io/lennett/pen/LYxQrOW ，在右下角按 `Fork` 按鈕複製 Pen。
