# 洛达什 _。forEach()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-foreach-method/](https://www.geeksforgeeks.org/lodash-_-foreach-method/)

**_。forEach()** **方法**迭代集合的元素，并为每个元素调用迭代。

**语法:**

```
_.forEach( collection, [iteratee = _.identity] )

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **集合:**此参数保存要迭代的集合。
*   **迭代:**是每次迭代调用的函数。

**返回值:**此方法返回集合。

**注意:**这里，const _ = require('lodash ')用于将 lodash 库导入文件。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.forEach() method 
_.forEach(['c', 'cpp', 'java','python'], function(value) {
  console.log(value);
});
```

**输出:**

```
'c'
'cpp'
'java'
'python'
['c', 'cpp', 'java','python']

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.forEach() method 
_.forEach({ 'x': 1, 'y': 2 }, function(value, key) {
  console.log(key);
});
```

**输出:**

```
'x'
'y'
{ 'x': 1, 'y': 2 }

```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash。

**参考:**T2】https://lodash.com/docs/4.17.15#forEach