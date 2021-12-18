# 洛达什 _。isArguments()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isarguments-method/](https://www.geeksforgeeks.org/lodash-_-isarguments-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、lang、函数、对象、数字等。

**_。isArguments()方法**检查值是否可能是参数对象。

**语法:**

```
_.isArguments(value)
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **值:**是用来校验值的函数。

**返回值:**如果值是参数对象，则该方法返回真，否则返回假。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Using the _.isArguments() method
let argu = _.isArguments(function() 
    { return arguments; } ());

// Printing the output 
console.log(argu);
```

**输出:**

```
true

```

**例 2:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var object = _.isArguments([ 7, 7, 8 ]);

// Using the _.isArguments() method
let argu = _.isArguments();

// Printing the output 
console.log(argu);
```

**输出:**

```
false

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。