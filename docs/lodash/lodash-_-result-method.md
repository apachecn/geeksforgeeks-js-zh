# 洛达什 _。结果()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-result-method/](https://www.geeksforgeeks.org/lodash-_-result-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。result()** 方法用于返回解析后的值。如果解析出的值是一个函数，那么它将通过其父对象的*这个*绑定来调用。几乎和 _。get()函数。

**语法:**

```
_.result( object, path, defaultValue )
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **对象:**是被查询的对象。
*   **路径:**是要解析的属性的路径的字符串或数组。
*   **默认值:**为未定义的解析值返回的值。它是一个可选值。

**返回值:**该方法返回解析值。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// The source object
var obj = 
  { 'x': [{ 'y': {
    'z1': 6, 'z2': _.constant(9) } }]
  };

// Use of _.result method 
console.log(_.result(obj, 'x[0].y.z1'));
console.log(_.result(obj, 'x[0].y.z2'));
```

**输出:**

```
6
9
```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// The source object
var obj =
  { 'x': [{ 'y': {
    'z1': 3, 'z2': _.constant(4) } }]
  };

// Use of _.result method 
console.log(
  _.result(obj, 'x[0].y.z3',
    'default')
);
console.log(
  _.result(obj, 'x[0].y.z3',
    _.constant('new-default'))
);
```

**输出:**

```
'default'
'new-default'

```