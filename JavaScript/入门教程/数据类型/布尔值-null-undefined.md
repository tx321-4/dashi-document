# null, undefined 和布尔值
在线教程：[null, undefined 和布尔值](https://wangdoc.com/javascript/types/null-undefined-boolean.html)
>创建时间：2021.07.29  
>更新时间：2021.07.29

## <a name="chapter-one" id="chapter-one"></a>一 目录
 

| 目录             | 
| ------------------ | 
| [一 目录](#chapter-one)               |
| [二 null 和 undefined](#chapter-two)               |
| &emsp;[2.1 概述](#chapter-two-one) |
| &emsp;[2.2 用法和含义](#chapter-two-two) |
| [三 布尔值](#chapter-three)           |



## <a name="chapter-two" id="chapter-two"></a>二 null 和 undefined
> [返回目录](#chapter-one)  

* 概述
* 用法和含义

### <a name="chapter-two-one" id="chapter-two-one"></a>2.1 概述

* `null`与`undefined` 都可以表示“没有”,含义非常相似。
* 在`if` 语句中，它们都会被自动转为`false`
* 转为数值(Number) 不同
```javascript
  Number(null) // 0
  5 + null // 5

  Number(undefined) // NaN
  5 + undefined // NaN
```


### <a name="chapter-two-two" id="chapter-two-two"></a>2.2 用法和含义
* `null`表示空值，即该处的值现在为空。用法如下
  * 调用函数时，某个参数未设置任何值，这时就可以传入`null`，表示该参数为空。
  * 某个函数接受引擎抛出的错误作为参数，如果运行过程中未出错，那么这个参数就会传入`null`,表示为发生错误
* `undefined` 表示 “未定义”, 场景如下
```javascript
// 变量声明，但没有赋值
var i;
i // undefined

//调用函数时，应该提供的参数没有提供，该参数等于 undefined

function f(x) {
  return x;
}
f() // undefined

// 对象没有赋值的属性
var o = new Obejct();
o.p // undefined

// 函数没有返回值时， 默认返回 undefined
function f(){}
f() // undefined
```




## <a name="chapter-three" id="chapter-three"></a>三 布尔值
> [返回目录](#chapter-one)  

布尔值代表“真”和“假”两个状态。“真”用关键词 `true` 表示， “假”用关键词`false` 表示。布尔值 只有这两个值。  
下列运算符会返回布尔值：
  * 前置逻辑运算符： `！`(Not)
  * 相等运算符：`===`、`!==`、`==`、`!=`
  * 比较运算符：`>`、`>=`、`<`、`<=`

如果JavaScript 预期某个位置应该是布尔值，会将该位置上现有的值自动转为布尔值。  
转换规则是除了下面六个值转为`false`,其余值都视为`true`。
* undefined
* null
* false
* 0
* NaN
* ”“ 和‘’（空字符串）

布尔值通常用于程序流程的控制
```javascript
if('') {
  console.log('true')
}
// 没有任何输出
```

空数组`[]` 和空对象`{}` 对应的布尔值,都是 `true`
```javascript
if({}){
  console.log('true');
}
// true

if([]){
  console.log('true');
}
// true
```
