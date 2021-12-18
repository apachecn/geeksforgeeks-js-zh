# 洛达什 _。setWith()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-setwith-method/](https://www.geeksforgeeks.org/lodash-_-setwith-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、lang、函数、对象、数字等。

**_。setWith()方法**类似于 _。set()方法，除了它接受被调用来产生 path 对象的定制器。如果定制器返回未定义的路径，则由方法来处理创建。

**语法:**

```
_.setWith(object, path, value, customizer)
```

**参数:**该方法接受上述和下述四个参数:

*   **对象:**是修饰对象的函数。
*   **路径:**设置属性的路径。
*   **值:**用于设置值。
*   **定制器:**是定制赋值的功能。

**返回值:**该方法返回对象。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var object = {};

// Using the _.setWith() method
let st_elem = _.setWith(object, 
        '[0][3]', 'd', Object);

// Printing the output 
console.log(st_elem);
```

**输出:**

```
{ '0': { '3': 'd' } }

```

**例二:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var object = {};

// Using the _.setWith() method
let st_elem = _.setWith(object, 
    '[0][1][2]', 'a', Object);

// Printing the output 
console.log(st_elem);
```

**输出:**

```
{ '0': {'1': { '2': 'a' } } }

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。