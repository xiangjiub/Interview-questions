## doctype(文档类型) 的作用是什么
总之，加上doctype声明，让浏览器使用标准模式、W3C标准

## HTML 和 XHTML 有什么区别？
HTML是超文本标记语言（Hyper Text Markup Language）的首字母缩略词，
超文本：超文本简单的意思就是“文本内的文本”。文本中有链接，是超文本。每次单击一个链接来打开一个新网页时，都是单击一个超文本来完成的。

标记语言：标记语言是一种编程语言，用于使文本更具交互性和动态性。它可以将文本转换为图像，表格，链接等。

XHTML代表可扩展超文本标记语言。它是HTML和XML语言之间的交叉

尽管XHTML与HTML几乎相同，但正确创建代码更为重要，因为XHTML在语法和区分大小写方面比HTML更严格严谨。XHTML文档是格式良好的，并使用标准XML解析器进行解析，这与HTML不同，HTML需要宽松的HTML特定解析器。

文档结构的变化
1、所有文件都必须有DOCTYPE。

2、中的xmlns属性是必需的，必须为文档指定xml命名空间。

3、结束标记是必须的
## 请描述 BFC(Block Formatting Context) 及其如何工作？
BFC定义：

BFC(Block formatting context)直译为"块级格式化上下文"。它是一个独立的渲染区域，只有Block-level box参与， 它规定了内部的Block-level Box如何 布局，并且与这个区域外部毫不相干。


BFC布局规则

1、内部的Box会在垂直方向，一个接一个地放置。

2、Box垂直方向的距离由margin决定。属于同一个BFC的两个相邻Box的margin会发生重叠。

3、每个元素的margin box的左边，与容器块border box的左边相接触(对于从左往右的格式化，否则相反)。即使存在浮动也是如此。

4、BFC就是页面上的一个隔离的独立容器，容器里面的子元素不会影响到外面的元素，反之亦然。

5、计算BFC的高度时，考虑BFC所包含的所有元素，连浮动元素也参与计算。

6、浮动的BOX区域不叠加到BFC上。

哪些元素会生成BFC?

1、根元素

2、float属性不为none

3、position为absolute或fixed

4、display为inline-block, table-cell, table-caption, flex, inline-flex

5、overflow不为visible