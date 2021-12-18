# 洛达什 _。方法()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-methodof-method/](https://www.geeksforgeeks.org/lodash-_-methodof-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

洛达什 **_。methodOf()方法**创建一个函数，在对象的给定路径上调用该方法。任何额外的参数都被提供给被调用的方法。

**语法:**

```
_.methodOf(object, args)

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **对象:**这是要查询的对象。
*   **参数:**这些是调用方法的参数。

**返回值:**这个方法返回新的调用者函数。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");              

// Use of _.methodOf() method 
var array = _.times(4, _.constant),
    object = 
        { 
            'www': array, 
            'geeks': array, 
            'for': array ,
            'geek':array
        };

gfg = _.map(['geeks[1]', 
    'geek[2]'], _.methodOf(object));

// Printing the output  
console.log(gfg);
```

**输出:**

```
[1, 2]

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");              

// Use of _.methodOf() method 
var array = _.times(4, _.constant),
    object = 
        { 
            'www': array, 
            'geeks': array, 
            'for': array ,
            'geek':array
        };

gfg = _.map([['www', '1'], ['for', 
    '0']], _.methodOf(object));

// Printing the output  
console.log(gfg);
```

**输出:**

```
[1, 0]

```