# 洛达什 _。省略()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-omit-method/](https://www.geeksforgeeks.org/lodash-_-omit-method/)

Lodash 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。省略()**方法用于返回对象的副本，该副本由给定对象的自身和继承的可枚举属性路径组成，这些路径没有被省略。它与 _。pick()方法。

**语法:**

```
_.omit( object, paths )
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **对象:**此参数保存源对象。
*   **路径:**此参数保存要省略的属性路径。

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

// Using the _.omit() method 
console.log(_.omit(obj, ['password', 'username']));
```

**输出:**

```
{Name: "GeeksforGeeks"}
```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// The source object
var obj = { 'x': 1, 'y': '2', 'z': 3 };

// Use the _.omit() method 
console.log(_.omit(obj, ['x', 'y']));
```

**输出:**

```
{'z': 3}
```