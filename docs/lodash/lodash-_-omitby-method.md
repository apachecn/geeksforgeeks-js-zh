# 洛达什 _。omitBy()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-omitby-method/](https://www.geeksforgeeks.org/lodash-_-omitby-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。omitBy()** 方法用于返回对象的副本，该副本由谓词不返回 truthy 的对象的自身和继承的可枚举字符串键控属性组成。它与 _ 相反。pickBy()方法。

**语法:**

```
_.omitBy( object, predicate )
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **对象:**此参数保存源对象。
*   **谓词:**该参数保存为每个属性调用的函数。它是一个可选值。

**返回值:**该方法返回新对象。

**例 1:**

## Javascript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// The source object
var obj = {
    Name: "GeeksforGeeks",
    password: 123456,
    username: "your_geeks"
 }

// Using the _.omitBy() method
console.log(_.omitBy(obj, _.isLength));
```

**输出:**

```
{Name: "GeeksforGeeks", username: "your_geeks"}
```

**例 2:**

## 【JavaScript】

```
// Requiring the lodash library 
const _ = require("lodash"); 

// The source object
var obj = { 'x': 1, 'y': '2', 'z': 3 };

// Using the _.omitBy() method
console.log(_.omitBy(obj, _.isNumber));
```

**输出:**

```
{'y': '2'}
```