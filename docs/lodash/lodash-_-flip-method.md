# 洛达什 _。翻转()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-flip-method/](https://www.geeksforgeeks.org/lodash-_-flip-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。flip()** **方法**用于创建一个函数，该函数调用给定的*函数*参数，其参数反转。

**语法:**

```
_.flip( func )

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **func:** 此参数保存接受一些参数的函数。

**返回值:**该方法返回新的翻转函数。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

function Func(a, b) { 
    return b + " is " + a;
} 

// Using the _.flip() method  
var gfg = _.flip(Func); 

console.log(
  gfg("GeeksforGeeks",
      "A Computer Science Portal for Geeks")
);
```

**输出:**

```
"GeeksforGeeks is A Computer Science Portal for Geeks"

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Using the _.flip() method 
var flipped = _.flip(function() {
  return _.toArray(arguments);
});

console.log(
  flipped('c', 'cpp', 'java', 'python')
);
```

**输出:**

```
['python', 'java', 'cpp', 'c']

```