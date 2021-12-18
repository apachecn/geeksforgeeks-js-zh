# 洛达什 _。比较器()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-comparator-method/](https://www.geeksforgeeks.org/lodash-_-comparator-method/)

洛达什 **_。comparator()** 方法取一个类似二元谓词的函数，返回一个 comparator 函数，可以作为 _ 的回调函数。sort()方法等。

**语法:**

```
_.comparator( function );

```

**参数:**该方法接受上面列出并在下面讨论的单个参数。

*   **函数:**是一个类似谓词的已定义函数。

**返回值:**这个方法返回一个比较器函数。

**注意:**要执行以下示例，您必须使用此命令提示符安装 **lodash-contrib** 库，并执行以下命令。

```
npm install lodash-contrib

```

以下示例说明了 Lodash _。JavaScript 中的 comparator()方法:

**示例 1:** 使用比较器功能进行排序。

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

var gfgFun = function(x, y) { 
    // Returns -1, 0 or 1
    return x <= y; 
};

// Array 
var arr = [4, 8, 2, 9, 1];

var comp = _.comparator(gfgFun);
// Using comparator function with _.sort() method
arr.sort(comp);

console.log("Sorted Array :",arr)
```

**输出:**

```
Sorted Array : [ 1, 2, 4, 8, 9 ]

```

**示例 2:** 使用比较器功能进行反向排序。

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

var gfgFun = function(x, y) { 
    // Returns -1, 0 or 1
    return x >= y; 
};

// Array 
var arr = [1, 10, 2, 9, 1];

var comp = _.comparator(gfgFun);
// Using comparator function with _.sort() method
arr.sort(comp);

console.log("Sorted Array :",arr)
```

**输出:**

```
Sorted Array : [ 10, 9, 2, 1, 1 ]

```