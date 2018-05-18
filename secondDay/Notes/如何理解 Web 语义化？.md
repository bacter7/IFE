如何理解 Web 语义化？

1. 语义化的原因

   > 让机器可以读懂内容

2. 顾轶灵的Semantic HTML 

   > http://justineo.github.io/slideshows/semantic-html/#/

   1. WWW

      > 1. 全称World Wide Web,别名（Web，万维网）
      > 2. 资源的网络
      >    * 定位（URL）
      >    * 访问（HTTP）
      >    * 导航（超文本）

   2. HTML 

      > 1. 万维网的发布语言（the publishing language of the World Wide Web）
      >
      > 2. 可以用来
      >
      >    - 发布文档（文本，表格，列表，...）
      >
      >    - 通过超链接获取信息
      >    - 建立用来访问远程服务的表单
      >    - 发布Web应用
      >
      > 3. 万维网的【粘合剂】
      >
      > 4. HTML最终由机器读取解析，或进行渲染，或挖掘出有用的信息为其他应用提供支持。

   3. HTML 语义    **元素+属性+属性值（+文档结构）**

      > 1. 全局属性
      >
      >     1. id属性
      >
      >        > 标示符（用于引用），不应依赖其语义处理相应元素
      >
      >     	2. `class`属性
      >
      >        > 鼓励使用描述内容本质的值
      >
      >     	3. `title`属性
      >
      >        > - 链接 - 描述目标信息
      >        > - 图片 - 版权/描述
      >        > - 引用 - 来源信息
      >        > - 交互元素 - 操作指南
      >
      >     	4. `lang`属性
      >
      >        > 内容使用的语义 【目测是language的缩写】
      >
      > 2. 元数据（metadata）
      >
      >    1. `head`元素
      >
      >       > 存放元数据的容器
      >
      >    2. `title`元素
      >
      >       > 存在于head中时，是文档对外的标题展示
      >       >
      >       > - 窗口标题
      >       > - 历史记录
      >       > - 搜索结果标题
      >
      >    3. `meta`元素
      >
      >       > | 属性                  | 值                                                           | 描述                                         |
      >       > | --------------------- | ------------------------------------------------------------ | -------------------------------------------- |
      >       > | charset(HTML5新特性)  | character_set                                                | 定义文档的字符编码                           |
      >       > | content               | text                                                         | 定义与 http-equiv 或 name 属性相关的元信息。 |
      >       > | http-equiv            | content-type <br/>expires<br/>refresh<br/>set-cookie         | 把 content 属性关联到 HTTP 头部。            |
      >       > | name                  | author<br/>description<br/>keywords<br/>generator<br/>revised<br/>others | 把 content 属性关联到一个名称。              |
      >       > | scheme（HTML5不支持） | format/URI                                                   | 定义用于翻译 content 属性值的格式。          |
      >       >
      >       > 
      >       >
      >       > 
      >
      > 3. 链接（links）
      >
      >    > 1. 链接类型
      >    >
      >    >    > - 外部资源链接，指向用来组成当前文档的外部资源，通常由UA（user agent）自动处理
      >    >    >
      >    >    > - 超链接，用来【导航】到其他资源（可以在UA中打开，下载）
      >    >    >
      >    >    >   元素：`link`（链接外部资源，如css,js）,`a`,`area`（地图中用到）
      >    >    >
      >    > 2. 链接
      >    >    >
      >    >    >   1. `link`
      >    >    >      - 元数据，用来描述文档本身与其他资源的关系
      >    >    >      - 必须包含rel（当前文档与被链接文档之间的关系）及href（被链接文档的位置）属性
      >    >    >   2. `a` 
      >    >    >      - 存在href属性时为超链接
      >    >    >      - 缺少href属性时为链接占位符
      >    >    >      - *与**link**元素不同，**a**元素代表的超链接都是显示的*
      >    >
      >
      > 4. 区块（`sections`）[区块实例](http://justineo.github.io/slideshows/semantic-html/#/6/9)
      >
      >    > 1. `article`元素
      >    >
      >    >    > - 独立的文档、页面、应用、站点
      >    >    > - 可以单独发布、重用
      >    >    > - 可以是...
      >    >    >   - 一篇帖子
      >    >    >   - 一篇文章
      >    >    >   - 一则用户评论
      >    >    >   - 一个可交互的widget
      >    >
      >    > 2. `section`元素
      >    >
      >    >    > - 按主题将内容分组，通常会有标题（heading）
      >    >    > - 并非【语义化的**div**】
      >    >    > - 当你希望这个元素的内容体现在文档的提纲中时，用section是合适的。
      >    >
      >    > 3. `nav`元素
      >    >
      >    >    > ```html
      >    >    > <nav>
      >    >    >   <ul>
      >    >    >     <li><a href="/">Home</a></li>
      >    >    >     <li><a href="/news">News</a></li>
      >    >    >     <li><a>Examples</a></li>
      >    >    >   </ul>
      >    >    > </nav>
      >    >    > ```
      >    >    >
      >    >    > - 可以帮助UA迅速获得导航内容
      >    >    > - 不一定要包含 `ul`，也可用自然文本进行导航。 
      >    >
      >    > 4. `aside`元素
      >    >
      >    >    > 补充信息，可以与内容相关，也可与内容无关，比如*广告*
      >    >
      >    > 5. `h`系列
      >    >
      >    >    > 标题h1-h6
      >    >
      >    > 6. `header`元素
      >    >
      >    >    > 我理解为页头元素
      >    >    >
      >    >    > - 一般存放导航信息（目录、搜索框、logo、）
      >    >
      >    > 7. `footer`元素
      >    >
      >    >    > 我理解为页脚元素
      >    >    >
      >    >    > - 一般是作者信息、相关文档、版权信息
      >    >    >
      >    >    > ```html
      >    >    > <footer><!-- site footer -->
      >    >    >   <nav>
      >    >    >     <p>
      >    >    >       <a href="/credits.html">Credits</a> —
      >    >    >       <a href="/tos.html">Terms of Service</a> —
      >    >    >       <a href="/index.html">Blog Index</a>
      >    >    >     </p>
      >    >    >   </nav>
      >    >    >   <p>Copyright © 2009 Gordon Freeman</p>
      >    >    > </footer>
      >    >    > ```
      >    >
      >    > 8. `address` 
      >    >
      >    >    > 联系人的相关信息信息 
      >
      > 5. 分组内容
      >
      >    > 1. `P`元素
      >    >
      >    >    > - [段落]的显示表述
      >    >
      >    > 2. `hr` 元素
      >    >
      >    >    > h5中不在有样式，h5之前有样式
      >    >
      >    > 3. pre元素
      >    >
      >    >    > 页面展示格式与输入时一致，空格等特殊符号不需要用符号实体也会直接显示
      >    >
      >    > 4. blockquote元素
      >    >
      >    >    > - 内容为引用
      >    >    > - `cite` 属性表示该来源的 URL
      >    >    > - 署名必须放在 `blockquote` 外
      >    >    >
      >    >    > ```html
      >    >    > <p>His next piece was the aptly named <cite>Sonnet 130</cite>:</p>
      >    >    > <blockquote cite="http://quotes.example.org/s/sonnet130.html">
      >    >    >   <p>My mistress' eyes are nothing like the sun,<br>
      >    >    >   Coral is far more red, than her lips red,<br>
      >    >    >   [...]</p>
      >    >    > </blockquote>
      >    >    > ```
      >    >
      >    > 5. `ol`,`ul`,`li`
      >    >
      >    >    > - 有序/无序列表
      >    >    > - `ol`下`li`元素的value属性代表该序列表向的序号值
      >    >    >
      >    >    > ```html
      >    >    > <p>Relegation zone:</p>
      >    >    > <ol>
      >    >    > <li value="18">Bolton Wanderers</li>
      >    >    > <li>Blackburn Rovers</li>
      >    >    > <li>Wolverhampton Wanderers</li>
      >    >    > </ol>
      >    >    > ```
      >    >
      >    > 6. `dl`,`dt`,`dd`
      >    >
      >    >    > - 名值对的集合
      >    >    > - 术语定义表 / 元数据（不知道是什么意思） / FAQ / ...
      >    >    >
      >    >    > ```html
      >    >    > <dl>
      >    >    >   <dt><dfn>happiness</dfn></dt>
      >    >    >   <dd class="part-of-speech"><i><abbr>n.</abbr></i></dd>
      >    >    >   <dd>The state of being happy.</dd>
      >    >    >   <dd>Good fortune; success. <q>Oh <b>happiness</b>! It worked!</q></dd>
      >    >    >   <dt><dfn>rejoice</dfn></dt>
      >    >    >   <dd><i class="part-of-speech"><abbr>v.intr.</abbr></i> To be delighted oneself.</dd>
      >    >    >   <dd><i class="part-of-speech"><abbr>v.tr.</abbr></i> To cause one to be delighted.</dd>
      >    >    > </dl>
      >    >    > ```
      >    >
      >    > 7. `figure`元素
      >    >
      >    >    > - 比较独立的、被引用的部分
      >    >    > - 通常内容与主题有关，
      >    >    > - 通常会有一个标题（`figcaption`）
      >    >    >   - `figcaption`元素
      >    >    >     - 图例、图表标题、代码说明...
      >    >
      >    > 8. `div`元素
      >    >
      >    >    > 最后的选择
      >    >
      >    > 9. `main`元素
      >    >
      >    >    > 唯一
      >
      > 6. 文本级语义
      >
      >    > 1. `em`元素
      >    >
      >    >    > - 标识侧重点的强调
      >    >    > - 视觉效果为斜体
      >    >
      >    > 2. `strong`元素
      >    >
      >    >    > - 标识内容的重要性
      >    >    > - 视觉效果为粗体
      >    >
      >    > 3. `i`元素
      >    >
      >    >    > - 表示另一种叙述方式
      >    >    >
      >    >    > - 视觉上是斜体
      >    >    >
      >    >    > - 建议与 `class` / `lang` 属性搭配使用
      >    >    >
      >    >    >   ```html
      >    >    >   <p>Sunflower (<i class="taxonomy">Helianthus annuus</i>) is an annual plant native to the Americas.</p>
      >    >    >   
      >    >    >   <p>There is a certain <i lang="fr">je ne sais quoi</i> in the air.</p>
      >    >    >   
      >    >    >   <p><i class="ship-name">Titanic</i> sank in the North Atlantic Ocean on 15 April 1912.</p>
      >    >    >   ```
      >    >
      >    > 4. `b`元素
      >    >
      >    >    > - 表示某种需要引起注意却又没有其他额外语义的内容
      >    >    >
      >    >    > - 视觉上是粗体
      >    >    >
      >    >    > - 建议与 `class` 属性搭配使用
      >    >    >
      >    >    >   ```html
      >    >    >   article>
      >    >    >     <h2>Kittens 'adopted' by pet rabbit</h2>
      >    >    >     <p><b class="lede">Six abandoned kittens have found an unexpected new mother figure — a pet rabbit.</b></p>
      >    >    >     <p>Veterinary nurse Melanie Humble took the three-week-old kittens to her Aberdeen home.</p>
      >    >    >   [...]
      >    >    >   ```
      >    >
      >    > 5. `small`元素
      >    >
      >    >    > - 一般是补充信息
      >    >    > - 视觉上是小字体
      >    >
      >    > 6. `s`元素
      >    >
      >    >    > - 视觉上*带删除线的文字*
      >    >    >
      >    >    > - 表示不再准确或不再相关的内容
      >    >    >
      >    >    > - 与 `del` 元素含义不同
      >    >    >
      >    >    >   ```html
      >    >    >   ¥ <strong>76.5</strong> <s>原价79.0</s>
      >    >    >   ```
      >    >
      >    > 7. `u`元素
      >    >
      >    >    > - 视觉上*带下划线的文字*
      >    >    >
      >    >    > - 表示用非文本进行的标注的内容
      >    >    >
      >    >    > - 中文转名/拼写检查的错误内容
      >    >    >
      >    >    >   ```html
      >    >    >   <u class="proper-name">屈原</u>放逐，乃賦<cite class="book-name">離騒</cite>。<u class="proper-name">左丘</u>失明，厥有<cite class="book-name">國語</cite>。（司馬遷《報任安書》）
      >    >    >   
      >    >    >   ```
      >    >
      >    > 8. `cite` 元素
      >    >
      >    >    > - 引述的作品标题
      >    >    >
      >    >    > - 书 / 论文 / 散文 / 电影 / 歌曲 / 电视节目 / 画作 / ...
      >    >    >
      >    >    >   ```html
      >    >    >   <p>My favorite movie is <cite>Transformers</cite> by Michael Bay.</p>
      >    >    >   ```
      >    >
      >    > 9. `q` 元素
      >    >
      >    >    > - 引用的来自其他来源的段内内容
      >    >    > - `cite` 属性表示该来源的 URL
      >    >    > - 不用 `q` 而用引号亦正确
      >    >
      >    > 10. `abbr` 元素
      >    >
      >    >     > - 其 `title` 属性的含义为所写的全称
      >    >     >
      >    >     > ```html
      >    >     > <p>The <abbr title="Web Hypertext Application Technology Working Group">WHATWG</abbr> started working on HTML5 in 2004.</p> 
      >    >     > ```
      >    >
      >    > 11. `dfn` 元素
      >    >
      >    >     > - 视觉上为斜体
      >    >     > - 展现一个定义实例
      >    >
      >    > 12. `time` 元素
      >    >
      >    >     > - 为表述的内容增加一个机器可读的时间数据
      >    >     >
      >    >     > - `datetime` 属性值必须是预定义的几种[时间格式](http://dev.w3.org/html5/spec/the-time-element.html#datetime-value)之一
      >    >     >
      >    >     > - 如果不含 `datetime` 属性，则会解析其文本内容值
      >    >     >
      >    >     >   ```htm
      >    >     >   <div class="vevent">
      >    >     >     <a class="url" href="http://www.web2con.com/">http://www.web2con.com/</a>
      >    >     >     <span class="summary">Web 2.0 Conference</span>:
      >    >     >     <time class="dtstart" datetime="2005-10-05">October 5</time> -
      >    >     >     <time class="dtend" datetime="2005-10-07">7</time>,
      >    >     >     at the <span class="location">Argent Hotel, San Francisco, CA</span>
      >    >     >   </div>
      >    >     >   ```
      >    >
      >    > 13. `code`, `samp`, `kbd` 元素
      >    >
      >    >     > 三个语义化元素
      >    >     >
      >    >     > - `code` - 代码片段
      >    >     > - `samp` - 计算机程序的输出
      >    >     > - `kbd` - 用户输入的内容 / 按键
      >    >
      >    > 14. `mark` 元素
      >    >
      >    >     > - 对内容进行标记
      >    >     >
      >    >     > - 视觉上会有背景色
      >    >
      >    > 15. `ruby`, `rt`, `rp` 元素
      >    >
      >    >     > - 注音标示，「ruby」来自日本印刷业
      >    >     >
      >    >     > - 主要于 CJK 文字
      >    >     >
      >    >     >   ```html
      >    >     >   <ruby>和<rp>(</rp><rt>hé</rt><rp>)</rp>谐<rp>(</rp><rt>xié</rt><rp>)</rp>社<rp>(</rp><rt>shè</rt><rp>)</rp>会<rp>(</rp><rt>huì</rt><rp>)</rp></ruby>
      >    >     >   ```
      >    >
      >    > 16. `span` 元素
      >    >
      >    >     > - 可以和 `class`, `lang` 等属性结合，为文本片段增加语义
      >    >     >
      >    >     > - 有更合适的元素时不应选择 `span`
      >    >     >
      >    >     >   ```html
      >    >     >   <span class="keyword">var</span> greet = <span class="function"><span class="keyword">function</span><span class="params">()</span> {
      >    >     >       console.log(<span class="string">"Hello world."</span>);
      >    >     >   }</span>
      >    >     >   ```
      >
      > 7. 更改记录
      >
      >    > 1. `ins`, `del` 元素
      >    >
      >    >    - 表示对当前文档内容进行的增添与删改
      >    >
      >    >    - `cite` 属性指向对某个修改的说明文档的 URL
      >    >
      >    >    - `datetime` 属性表示了修改发生的时间 ([取值规范](http://dev.w3.org/html5/spec/common-microsyntaxes.html#valid-date-string-with-optional-time))
      >    >
      >    >    - 用来记录文档的编辑历史
      >    >
      >    >      ```
      >    >      a dozen is <del>20</del> <ins>12</ins> pieces
      >    >      ```
      >
      > 8. 嵌入内容
      >
      >    > 1. `img` 元素
      >    >
      >    > 2. `iframe`, `embed`, `object`, `param` 元素
      >    >
      >    >    > - `iframe` - 内嵌的浏览上下文
      >    >    > - `embed` - 外部应用或可交互内容的整合入口
      >    >    > - `object` - 通用外部资源
      >    >    >   - 根据具体内容可以被处理为图片、内嵌的浏览上下文、供插件调用的资源
      >    >    > - `param` - 为 `object` 元素传递的参数
      >
      > 9. 表格数据
      >
      >    > 1. `table` 元素
      >    >
      >    >    > - 用来表示超过一维的数据
      >    >
      >    > 2. `caption` 元素
      >    >
      >    >    > - 表示所处的 `table` 的标题
      >    >
      >    > 3. `tbody`, `thead`, `tfoot` 元素
      >    >
      >    >    > - 均为一组表格行
      >    >    > - `thead` 表示列头 (通常为列标题，单元格用 `th` 元素)
      >    >    > - `tfoot` 表示列脚 (通常为列数据汇总)
      >    >
      >    > 4. `col`, `colgroup`, `tr` 元素
      >    >
      >    >    >  列，列组，行 
      >    >
      >    > 5. `td`, `th` 元素
      >    >
      >    >    > - `td` - 数据单元格
      >    >    > - `th` - 标题单元格

硬啃MDN

1. 块级元素和内联元素

   > 块级元素出现时单独占一行；而内联元素不会大致文本换行
   >
   > 块级元素同场展示 结构化的内容：例如，段落，列表，导航菜单，页脚等

2. 元素属性

   > 元素间多个属性时，通过**空格**隔开；格式如下，属性=“属性值”

3. <a> 是锚，超链接

   > href，链接地址；title，鼠标悬停链接上会有提示内容；target，链接打开方式，本页还是新页面

4. 分析HTML文档

   > - ```
   >   <!DOCTYPE html>
   >   <html>
   >     <head>
   >       <meta charset="utf-8">
   >       <title>My test page</title>
   >     </head>
   >     <body>
   >       <p>This is my page</p>
   >     </body>
   >   </html>
   >   ```
   >
   > - <!DOCTYPE html> ,声明文档类型，历史沿用保留
   >
   > - `<html></html>` ,整个页面的根元素
   >
   > - `<head></head> `，元素容器，包含的元素不在页面中显示
   >
   > - `<meta charset="utf-8">` ，用于说明的元素，此处说明文档使用utf-8字符集编码。
   >
   > - `<title></title>`，标签控制页面标题
   >
   > - `<body></body> `，元素容器，包含页面中显示的内容

5. 元数据 `<meta>`

   > 描述数据的数据，
   >
   > - name ,制定meta元素的类型，即包含的信息类型
   > - content，指定了实际的元数据内容



#### 写在最后：

MDN没有啃完，也没有看W3C，只是看***顾轶灵***的语义化就花了很久的实践，感觉就像是啃了以便W3的标签，有一点点收获吧，再接再厉，