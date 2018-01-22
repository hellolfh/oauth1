\# Editor.md

!\[\]\([https://pandao.github.io/editor.md/images/logos/editormd-logo-180x180.png\](https://pandao.github.io/editor.md/images/logos/editormd-logo-180x180.png\)\)

!\[\]\([https://img.shields.io/github/stars/pandao/editor.md.svg\](https://img.shields.io/github/stars/pandao/editor.md.svg\)\) !\[\]\([https://img.shields.io/github/forks/pandao/editor.md.svg\](https://img.shields.io/github/forks/pandao/editor.md.svg\)\) !\[\]\([https://img.shields.io/github/tag/pandao/editor.md.svg\](https://img.shields.io/github/tag/pandao/editor.md.svg\)\) !\[\]\([https://img.shields.io/github/release/pandao/editor.md.svg\](https://img.shields.io/github/release/pandao/editor.md.svg\)\) !\[\]\([https://img.shields.io/github/issues/pandao/editor.md.svg\](https://img.shields.io/github/issues/pandao/editor.md.svg\)\) !\[\]\([https://img.shields.io/bower/v/editor.md.svg\](https://img.shields.io/bower/v/editor.md.svg\)\)

\*\*目录 \(Table of Contents\)\*\*

\[TOCM\]

\[TOC\]

\# Heading 1

\#\# Heading 2

\#\#\# Heading 3

\#\#\#\# Heading 4

\#\#\#\#\# Heading 5

\#\#\#\#\#\# Heading 6

\# Heading 1 link \[Heading link\]\([https://github.com/pandao/editor.md](https://github.com/pandao/editor.md) "Heading link"\)

\#\# Heading 2 link \[Heading link\]\([https://github.com/pandao/editor.md](https://github.com/pandao/editor.md) "Heading link"\)

\#\#\# Heading 3 link \[Heading link\]\([https://github.com/pandao/editor.md](https://github.com/pandao/editor.md) "Heading link"\)

\#\#\#\# Heading 4 link \[Heading link\]\([https://github.com/pandao/editor.md](https://github.com/pandao/editor.md) "Heading link"\) Heading link \[Heading link\]\([https://github.com/pandao/editor.md](https://github.com/pandao/editor.md) "Heading link"\)

\#\#\#\#\# Heading 5 link \[Heading link\]\([https://github.com/pandao/editor.md](https://github.com/pandao/editor.md) "Heading link"\)

\#\#\#\#\#\# Heading 6 link \[Heading link\]\([https://github.com/pandao/editor.md](https://github.com/pandao/editor.md) "Heading link"\)

\#\#\#\# 标题（用底线的形式）Heading \(underline\)

This is an H1

=============

This is an H2

---

\#\#\# 字符效果和横线等

---

~~删除线~~ &lt;s&gt;删除线（开启识别HTML标签时）&lt;/s&gt;

\*斜体字\*      \_斜体字\_

\*\*粗体\*\*  \_\_粗体\_\_

\*\*\*粗斜体\*\*\* \_\_\_粗斜体\_\_\_

上标：X&lt;sub&gt;2&lt;/sub&gt;，下标：O&lt;sup&gt;2&lt;/sup&gt;

\*\*缩写\(同HTML的abbr标签\)\*\*

&gt; 即更长的单词或短语的缩写形式，前提是开启识别HTML标签时，已默认开启

The &lt;abbr title="Hyper Text Markup Language"&gt;HTML&lt;/abbr&gt; specification is maintained by the &lt;abbr title="World Wide Web Consortium"&gt;W3C&lt;/abbr&gt;.

\#\#\# 引用 Blockquotes

&gt; 引用文本 Blockquotes

引用的行内混合 Blockquotes

&gt; 引用：如果想要插入空白换行\`即&lt;br /&gt;标签\`，在插入处先键入两个以上的空格然后回车即可，\[普通链接\]\([http://localhost/\)。](http://localhost/%29。)

\#\#\# 锚点与链接 Links

\[普通链接\]\([http://localhost/\](http://localhost/\)\)

\[普通链接带标题\]\([http://localhost/](http://localhost/) "普通链接带标题"\)

直接链接：&lt;[https://github.com&gt](https://github.com&gt);

\[锚点链接\]\[anchor-id\]

\[anchor-id\]: [http://www.this-anchor-link.com/](http://www.this-anchor-link.com/)

\[mailto:test.test@gmail.com\]\(mailto:test.test@gmail.com\)

GFM a-tail link @pandao  邮箱地址自动链接 test.test@gmail.com  www@vip.qq.com

&gt; @pandao

\#\#\# 多语言代码高亮 Codes

\#\#\#\# 行内代码 Inline code

执行命令：\`npm install marked\`

\#\#\#\# 缩进风格

即缩进四个空格，也做为实现类似 \`&lt;pre&gt;\` 预格式化文本 \( Preformatted Text \) 的功能。

```
&lt;?php

    echo "Hello world!";

?&gt;
```

预格式化文本：

```
\| First Header  \| Second Header \|

\| ------------- \| ------------- \|

\| Content Cell  \| Content Cell  \|

\| Content Cell  \| Content Cell  \|
```

\#\#\#\# JS代码

\`\`\`javascript

function test\(\) {

```
console.log\("Hello world!"\);
```

}

\(function\(\){

```
var box = function\(\) {

    return box.fn.init\(\);

};



box.prototype = box.fn = {

    init : function\(\){

        console.log\('box.init\(\)'\);



        return this;

    },



    add : function\(str\) {

        alert\("add", str\);



        return this;

    },



    remove : function\(str\) {

        alert\("remove", str\);



        return this;

    }

};



box.fn.init.prototype = box.fn;



window.box =box;
```

}\)\(\);

var testBox = box\(\);

testBox.add\("jQuery"\).remove\("jQuery"\);

\`\`\`

\#\#\#\# HTML 代码 HTML codes

\`\`\`html

&lt;!DOCTYPE html&gt;

&lt;html&gt;

```
&lt;head&gt;

    &lt;mate charest="utf-8" /&gt;

    &lt;meta name="keywords" content="Editor.md, Markdown, Editor" /&gt;

    &lt;title&gt;Hello world!&lt;/title&gt;

    &lt;style type="text/css"&gt;

        body{font-size:14px;color:\#444;font-family: "Microsoft Yahei", Tahoma, "Hiragino Sans GB", Arial;background:\#fff;}

        ul{list-style: none;}

        img{border:none;vertical-align: middle;}

    &lt;/style&gt;

&lt;/head&gt;

&lt;body&gt;

    &lt;h1 class="text-xxl"&gt;Hello world!&lt;/h1&gt;

    &lt;p class="text-green"&gt;Plain text&lt;/p&gt;

&lt;/body&gt;
```

&lt;/html&gt;

\`\`\`

\#\#\# 图片 Images

Image:

!\[\]\([https://pandao.github.io/editor.md/examples/images/4.jpg\](https://pandao.github.io/editor.md/examples/images/4.jpg\)\)

&gt; Follow your heart.

!\[\]\([https://pandao.github.io/editor.md/examples/images/8.jpg\](https://pandao.github.io/editor.md/examples/images/8.jpg\)\)

&gt; 图为：厦门白城沙滩

图片加链接 \(Image + Link\)：

\[!\[\]\([https://pandao.github.io/editor.md/examples/images/7.jpg\)\]\(https://pandao.github.io/editor.md/images/7.jpg](https://pandao.github.io/editor.md/examples/images/7.jpg%29]%28https://pandao.github.io/editor.md/images/7.jpg) "李健首张专辑《似水流年》封面"\)

&gt; 图为：李健首张专辑《似水流年》封面

---

\#\#\# 列表 Lists

\#\#\#\# 无序列表（减号）Unordered Lists \(-\)

* 列表一

* 列表二

* 列表三

\#\#\#\# 无序列表（星号）Unordered Lists \(\*\)

\* 列表一

\* 列表二

\* 列表三

\#\#\#\# 无序列表（加号和嵌套）Unordered Lists \(+\)

* 列表一

* 列表二

  * 列表二-1

  * 列表二-2

  * 列表二-3

* 列表三

  \* 列表一

  \* 列表二

  \* 列表三

\#\#\#\# 有序列表 Ordered Lists \(-\)

1. 第一行

2. 第二行

3. 第三行

\#\#\#\# GFM task list

* \[x\] GFM task list 1

* \[x\] GFM task list 2

* \[ \] GFM task list 3

  * \[ \] GFM task list 3-1

  * \[ \] GFM task list 3-2

  * \[ \] GFM task list 3-3

* \[ \] GFM task list 4

  * \[ \] GFM task list 4-1

  * \[ \] GFM task list 4-2

---

\#\#\# 绘制表格 Tables

\| 项目        \| 价格   \|  数量  \|

\| --------   \| -----:  \| :----:  \|

\| 计算机      \| $1600   \|   5     \|

\| 手机        \|   $12   \|   12   \|

\| 管线        \|    $1    \|  234  \|

First Header  \| Second Header

------------- \| -------------

Content Cell  \| Content Cell

Content Cell  \| Content Cell

\| First Header  \| Second Header \|

\| ------------- \| ------------- \|

\| Content Cell  \| Content Cell  \|

\| Content Cell  \| Content Cell  \|

\| Function name \| Description                    \|

\| ------------- \| ------------------------------ \|

\| \`help\(\)\`      \| Display the help window.       \|

\| \`destroy\(\)\`   \| \*\*Destroy your computer!\*\*     \|

\| Left-Aligned  \| Center Aligned  \| Right Aligned \|

\| :------------ \|:---------------:\| -----:\|

\| col 3 is      \| some wordy text \| $1600 \|

\| col 2 is      \| centered        \|   $12 \|

\| zebra stripes \| are neat        \|    $1 \|

\| Item      \| Value \|

\| --------- \| -----:\|

\| Computer  \| $1600 \|

\| Phone     \|   $12 \|

\| Pipe      \|    $1 \|

---

\#\#\#\# 特殊符号 HTML Entities Codes

© &  ¨ ™ ¡ £

& &lt; &gt; ¥ € ® ± ¶ § ¦ ¯ « ·

X² Y³ ¾ ¼  ×  ÷   »

18ºC  "  '

\[========\]

\#\#\# Emoji表情 :smiley:

&gt; Blockquotes :star:

\#\#\#\# GFM task lists & Emoji & fontAwesome icon emoji & editormd logo emoji :editormd-logo-5x:

* \[x\] :smiley: @mentions, :smiley: \#refs, \[links\]\(\), \*\*formatting\*\*, and &lt;del&gt;tags&lt;/del&gt; supported :editormd-logo:;

* \[x\] list syntax required \(any unordered or ordered list supported\) :editormd-logo-3x:;

* \[x\] \[ \] :smiley: this is a complete item :smiley:;

* \[ \] \[\]this is an incomplete item \[test link\]\(\#\) :fa-star: @pandao;

* \[ \] \[ \]this is an incomplete item :fa-star: :fa-gear:;

  * \[ \] :smiley: this is an incomplete item \[test link\]\(\#\) :fa-star: :fa-gear:;

  * \[ \] :smiley: this is  :fa-star: :fa-gear: an incomplete item \[test link\]\(\#\);

\#\#\#\# 反斜杠 Escape

\_literal asterisks\_

\[========\]

\#\#\# 科学公式 TeX\(KaTeX\)

$$E=mc^2$$

行内的公式$$E=mc^2$$行内的公式，行内的$$E=mc^2$$公式。

$$x &gt; y$$

$$\\(\sqrt{3x-1}+\(1+x\)^2\\)$$

$$\sin\(\alpha\)^{\theta}=\sum\_{i=0}^{n}\(x^i + \cos\(f\)\)$$

多行公式：

\`\`\`math

\displaystyle

\left\( \sum\\_{k=1}^n a\\_k b\\_k \right\)^2

\leq

\left\( \sum\\_{k=1}^n a\\_k^2 \right\)

\left\( \sum\\_{k=1}^n b\\_k^2 \right\)

\`\`\`

\`\`\`katex

\displaystyle

```
\frac{1}{

    \Bigl\(\sqrt{\phi \sqrt{5}}-\phi\Bigr\) e^{

    \frac25 \pi}} = 1+\frac{e^{-2\pi}} {1+\frac{e^{-4\pi}} {

    1+\frac{e^{-6\pi}}

    {1+\frac{e^{-8\pi}}

     {1+\cdots} }

    } 

}
```

\`\`\`

\`\`\`latex

f\(x\) = \int\_{-\infty}^\infty

```
\hat f\(\xi\)\,e^{2 \pi i \xi x}

\,d\xi
```

\`\`\`

\#\#\# 分页符 Page break

&gt; Print Test: Ctrl + P

\[========\]

\#\#\# 绘制流程图 Flowchart

\`\`\`flow

st=&gt;start: 用户登陆

op=&gt;operation: 登陆操作

cond=&gt;condition: 登陆成功 Yes or No?

e=&gt;end: 进入后台

st-&gt;op-&gt;cond

cond\(yes\)-&gt;e

cond\(no\)-&gt;op

\`\`\`

\[========\]

\#\#\# 绘制序列图 Sequence Diagram

\`\`\`seq

Andrew-&gt;China: Says Hello

Note right of China: China thinks\nabout it

China--&gt;Andrew: How are you?

Andrew-&gt;&gt;China: I am good thanks!

\`\`\`

\#\#\# End

