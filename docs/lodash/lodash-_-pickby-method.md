# 洛达什 _。pickBy()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-pickby-method/](https://www.geeksforgeeks.org/lodash-_-pickby-method/)

Lodash 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。pickBy()** 方法用于返回由对象属性谓词返回的 truthy for 组成的对象的副本。

**语法:**

```
_.pickBy( object, predicate )
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

// Using the _.pickBy() method 
console.log(_.pickBy(obj, _.isLength));
```

**输出:**

```
{'password': 123456}
```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// The source object
var obj = { 'x': 1, 'y': '2', 'z': 3 };

// Using the _.pickBy() method 
console.log(_.pickBy(obj, _.isNumber));
```

**输出:**

```
{'x': 1, 'z': 3}
```