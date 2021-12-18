# 洛达什 _。cond()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-cond-method/](https://www.geeksforgeeks.org/lodash-_-cond-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。
The _。 **cond** 方法创建一个函数，该函数对进行迭代，并调用第一个谓词的相应函数来返回 truthy。谓词-函数对是用创建的函数的绑定和参数调用的。

**语法:**

```
_.cond(pairs)
```

**参数:**该方法接受一个参数，如上所述，如下所述:

*   **对:**【数组】谓词-函数对。

**返回值:**【数组】谓词-函数对。

**注意:**这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");

//  using _.cond() method
var func1 = _.cond([
    [_.matches({ 'geeks': 1 }),
        _.constant('Matches Geeks')],
    [_.conforms({ 'for': _.isNumber }),
        _.constant('Matches For')],
    [_.stubTrue, _.constant('no match')]
]);

// Storing the Result
gfg = func1({ 'geeks': 1, 'b': 2 });

// Printing the output  
console.log(gfg);
```

**输出:**

```
"Matches Geeks"
```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");

//  using _.cond() method
var func2 = _.cond([
    [_.matches({ 'geeks': 1 }), 
        _.constant('Matches Geeks')],
    [_.conforms({ 'for': _.isNumber }), 
        _.constant('Matches For')],
    [_.stubTrue, _.constant('No Match')]
]);

// Storing Result 
gfg1 = func2({ 'geeks': 0, 'for': 1 });
gfg2 = func2({ 'geeks': '1', 'for': '2' });

// Printing the output  
console.log(gfg1);
console.log(gfg2)
```

**输出:**

```
"Matches For"
"No Match"

```