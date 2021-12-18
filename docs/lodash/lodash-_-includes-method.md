# 洛达什 _。包括()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-includes-method/](https://www.geeksforgeeks.org/lodash-_-includes-method/)

**_。包括()** **方法**用于查找值是否在集合中。如果集合是一个字符串，将测试它的值子字符串，否则使用 SameValueZero()方法进行相等比较。如果给定的索引为负，则从集合的结束索引开始测试该值作为偏移量。

**语法:**

```
_.includes( collection, value, index )

```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **集合:**此参数保存要检查的集合。集合可以是数组、对象或字符串。
*   **值:**此参数保存要搜索的值。
*   **索引:**此参数保存要搜索的索引。

**返回值:**此方法返回 **true** 如果在集合中找到值，否则 **false** 。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Collection of string
var name = [ 'gfg', 'geeks', 'computer', 'science', 'portal' ];

// Check value is found or not by _.includes() method
console.log(_.includes(name, 'computer'));

// Check value is found or not by _.includes() method
console.log(_.includes(name, 'geeeks')); 

// Check value is found or not by _.includes() method
console.log(_.includes(name, 'gfg', 2));
```

**输出:**

```
true
false
false

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Collection of integer value
var name = [ 10, 15, 20, 25, 30 ]; 

// Check value is found or not by _.includes() method
console.log(_.includes(name, 25));

// Check value is found or not by _.includes() method
console.log(_.includes(name, 35));

// Check value is found or not by _.includes() method
console.log(_.includes(name, 25, 3));
```

**输出:**

```
true
false
true

```