# 洛达什 _。memoize()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-memoize-method/](https://www.geeksforgeeks.org/lodash-_-memoize-method/)

**_。memoize()** **方法**用于通过缓存函数计算的结果来记忆给定的函数。如果发出了解析器，则用于存储结果的缓存键将根据给 memoized 方法的参数来确定。默认情况下，提供给 memoized 函数的第一个参数用作映射缓存键。

**语法:**

```
_.memoize(func, [resolver])

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **函数:**该参数保持函数的输出被记忆。
*   **解析器:**是解析缓存键的功能。

**返回值:**该方法返回新的记忆函数。

**注意:**这里，const _ = require('lodash ')用于将 lodash 库导入文件。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.memoize() method  
var sum = _.memoize(function (n) { 
    return n < 1 ? n : n + sum(n - 1); 
}); 

// Sum of first 6 natural number  
console.log(sum(6));
```

**输出:**

```
21

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

var object = { 'cpp': 5, 'java': 8 };

// Use of _.memoize() method  
var values = _.memoize(_.values);

// value of object 
console.log(values(object)); 

// Modify the result cache.
values.cache.set(object, ['html', 'css']);
console.log(values(object));
```

**输出:**

```
[5, 8]
['html', 'css']

```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash。