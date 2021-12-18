# 洛达什 _。pick()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-pick-method/](https://www.geeksforgeeks.org/lodash-_-pick-method/)

Lodash 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。pick()** 方法用于返回由拾取的对象属性组成的对象副本。

**语法:**

```
_.pick( object, paths )

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **对象:**此参数保存源对象。
*   **路径:**此参数保存要拾取的属性路径。

**返回值:**该方法返回新对象。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// The source object
var obj = { 
    Name: "GeeksforGeeks", 
    password: "gfg@1234", 
    username: "your_geeks"
}

// Using the _.pick() method 
console.log(_.pick(obj, ['password', 'username']));
```

**输出:**

```
{password: "gfg@1234", username: "your_geeks"}

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// The source object
var obj = { 'x': 1, 'y': '2', 'z': 3 };

// Using the _.pick() method 
console.log(_.pick(obj, ['x', 'y']));
```

**输出:**

```
{x: 1, y: '2'}

```