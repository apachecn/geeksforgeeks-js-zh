# 洛达什 _。常数()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-constant-method/](https://www.geeksforgeeks.org/lodash-_-constant-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。_。常量方法用于创建函数创建返回值的函数。

**语法:**

```
_.constant(value)
```

**参数:**该方法接受一个参数，如上所述，如下所述:

*   **Value** : The value returned by the new function.

**返回值:**【函数】返回新的常量函数。

**例 1:**

```
// Requiring the lodash library  
const _ = require("lodash");    

// Using _.constant() method
let gfg = _.times(3, _.constant({ 'geeks': 3 }));

// Printing the output  
console.log(gfg);
```

**注意:**这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

**输出:**

```
[Object {geeks: 3}, Object {geeks: 3}, Object {geeks: 3}]
```

**例 2:**

```
// Requiring the lodash library  
const _ = require("lodash");    

// Using _.constant() method
let obj = _.times(2,  _.constant({ 'a': 5 }));

// Checking if both objects are same
let gfg = console.log(obj[0] === obj[1] )

// Printing the output  
console.log(gfg);
```

**注意:**这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

**输出:**

```
true
```