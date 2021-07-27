# Flex 弹性布局
>创建时间：2021.07.27  
>更新时间：2021.07.27

## 前言
> 简介： Flexible Box ,意为“弹性布局”，用来为盒模型提供最大的灵活性  
  
> 概念：采用Flex布局的元素,成为Flex容器，容器里的子元素自动成为容器成员，称为Flex项目
* 任何一个容器都可以指定为Flex布局
  * display: flex
* 行内元素也可以使用flex
  * display: inline-flex
* Webkit内核的浏览器，必须加上`-webkit`前缀
  * display:flex
  * diplay:-webkit-flex

>注意：设置Flex布局之后，子元素的`float`、`clear`、`vertical-align` 属性将失效

## <a name="chapter-one" id="chapter-one"></a>一 目录

| 文件名             | 存放内容                           |
| ------------------ | --------------------------------  |
| [一 目录](#chapter-one)            | 目录            |
| [二 容器](#chapter-two)               | 容器的属性         |
| &emsp;[2.1 flex-direction](#chapter-two-one) |  主轴的方向 |
| &emsp;[2.2 flex-wrap](#chapter-two-two) | 是否换行 |
| &emsp;[2.3 flex-flow](#chapter-two-three) | flex-direction、flex-wrap 简写 |
| &emsp;[2.4 justify-content](#chapter-two-four) | 项目的对齐方式 |
| &emsp;[2.5 align-items](#chapter-two-five) | 交叉轴上 对齐方式 |
| &emsp;[2.6 align-content](#chapter-two-six) | 多轴线 对齐方式 |
| [三 项目](#chapter-three)               | 项目的属性         |
| &emsp;[3.1 order](#chapter-three-one) |  项目的排列顺序 |
| &emsp;[3.2 flex-grow](#chapter-three-two) | 项目的放大比例 |
| &emsp;[3.3 flex-shrink](#chapter-three-three) | 项目的缩小比例 |
| &emsp;[3.4 flex-basis](#chapter-three-four) | 分配多余的空间 |
| &emsp;[3.5 flex](#chapter-three-five) | flex-grow、flex-shrink、flex-basis 的简写 |
| &emsp;[3.6 align-self](#chapter-three-six) | 不同于其他项目的对齐方式 |
| [四 参考链接](#chapter-four) | 参考链接|
## <a name="chapter-two" id="chapter-two"></a>二 容器
> [返回目录](#chapter-one)  
* flex-direction
* flex-wrap
* flex-flow
* justify-content
* align-items
* align-content

### <a name="chapter-two-one" id="chapter-two-one"></a>2.1 flex-direction
> [返回目录](#chapter-one)  

`flex-direction` 属性决定主轴的方向（即项目的排列方向）
  * row(默认值)：主轴为水平方向，起点在左端
  * row-reverse：主轴为水平方向，起点在右端
  * column：主轴为垂直方向，起点在上沿
  * column-reverse：主轴为垂直方向，起点在下沿

 ### <a name="chapter-two-two" id="chapter-two-two"></a>2.2 flex-wrap
> [返回目录](#chapter-one)  

`flex-wrap`属性定义，如果一条轴线排不下， 如何换行
  * nowrap(默认值)：不换行
  * wrap：换行，第一行在上方
  * wrap-reverse：换行，第一行在下方


 ### <a name="chapter-two-three" id="chapter-two-three"></a>2.3 flex-flow
> [返回目录](#chapter-one)  

`flex-flow` 属性是`flex-direction`属性和`flex-wrap`属性的简写形式，
  * row nowrap (默认值)

 ### <a name="chapter-two-four" id="chapter-two-four"></a>2.4 justify-content
> [返回目录](#chapter-one)  

`justify-content`属性 定义了项目在主轴上的对齐方式
  * flex-start（默认值）：左对齐
  * flex-end：右对齐
  * center：居中
  * space-between： 两端对齐，项目之间的间隔都相等
  * space-around：每个项目两侧的间隔相等。所以，项目之间的间隔比项目与边框的间隔大一倍

 ### <a name="chapter-two-five" id="chapter-two-five"></a>2.5 align-items
> [返回目录](#chapter-one)  

`align-items` 属性定义项目在交叉轴上如何对齐
  * flex-start：交叉轴的起点对齐
  * flex-end：交叉轴的终点对齐
  * center：交叉轴的中点对齐
  * baseline： 项目的第一行文字的基线对齐
  * stretch（默认值）：如何项目未设置高度或设为auto，将占满整个容器的高度
 ### <a name="chapter-two-six" id="chapter-two-six"></a>2.6 align-content
> [返回目录](#chapter-one)  

`align-content`属性定义了多跟轴线的对齐方式。如果项目只有一个轴线，该属性不起作用
  * flex-start：交叉轴的起点对齐
  * flex-end：交叉轴的终点对齐
  * center：交叉轴的中点对齐
  * space-between：与交叉轴两端对齐，轴线之间的间隔平均分布
  * space-around：每根轴线两侧的间隔相等。所以轴线之间的间隔比轴线与边框的间隔大一倍
  * stretch（默认值）：轴线占满整个交叉轴

## <a name="chapter-two" id="chapter-two"></a>三 项目
> [返回目录](#chapter-one)  
* order
* flex-grow
* flex-shrink
* flex-basis
* flex
* align-self

### <a name="chapter-three-one" id="chapter-three-one"></a>3.1 order
> [返回目录](#chapter-one)  

`order` 属性定义项目的排列顺序。数值越小，排列越靠前，默认为0

 ### <a name="chapter-three-two" id="chapter-three-two"></a>3.2 flex-grow
> [返回目录](#chapter-one)  

`flex-grow` 属性定义项目的放大比例，默认为0，即如果存在剩余空间，也不放大
* 如果所有项目的`flex-grow`属性都为1，则他们将等分剩余空间，如果一个项目的`flex-grow`属性为2，其他项目都为1，则前者占据的剩余空间将比其他项目多一倍

 ### <a name="chapter-three-three" id="chapter-three-three"></a>3.3 flex-shrink
> [返回目录](#chapter-one)  

`flex-shrink`属性定义了项目的缩小比例，默认我1，即如何空间不足，该项目将缩小

* 如果所有项目的`flex-shrink`属性都为1，当空间不足时，都将等比例缩小。如果一个项目的`flex-shrink`属性为0，其他项目都为1，则空间不足时， 前者不缩小
* 负值对该属性无效
* 
 ### <a name="chapter-three-four" id="chapter-three-four"></a>3.4 flex-basis
> [返回目录](#chapter-one)  

`flex-basis`属性定义了在分配多余空间之前，项目占据的主轴空间。浏览器根据这个属性，计算主轴是否有多余空间。它的默认值为`auto`，即 项目本来大小
* 它可以设为跟`width`或`height`属性一样的值，则项目将占据固定空间

 ### <a name="chapter-three-five" id="chapter-three-five"></a>3.5 flex
> [返回目录](#chapter-one)  

`flex`属性是`flex-grow`，`flex-shrink`和`flex-basis`的简写，默认值为`0 1 auto`。后两个属性可选
 ### <a name="chapter-three-six" id="chapter-three-six"></a>3.6 align-self
> [返回目录](#chapter-one)  

`align-self`属性允许单个项目有与其他项目不一样的对齐方式,可覆盖`align-items`属性。默认值为`auto`，表示继承父元素的`align-items`属性，如何没有父元素，则等同于`stretch`


## <a name="chapter-four" id="chapter-four"></a>四 参考链接
> [返回目录](#chapter-one)  
> 
* [x] [Flex 布局教程：语法篇](http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html)
* [x] [Flex 布局教程：实例篇](http://www.ruanyifeng.com/blog/2015/07/flex-examples.html)