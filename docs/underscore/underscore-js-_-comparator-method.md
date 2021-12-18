# 下划线. js _。比较器()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-比较器-方法/](https://www.geeksforgeeks.org/underscore-js-_-comparator-method/)

**_。comparator()** 方法取一个类似二元谓词的函数，返回一个 comparator 函数，可以作为 _ 的回调函数。sort()方法等。

**语法:**

```
_.comparator( function );
```

**参数:**

*   **函数:**定义的类似谓词的函数。

**返回值:**这个方法返回一个比较器函数。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**示例 1:** 使用比较器功能进行排序。

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var gfgFun = function(x, y) { 
    // Returns -1, 0 or 1
    return x <= y; 
};

// Array 
var arr = [4, 8, 2, 9, 1];

var comp = _.comparator(gfgFun);
// Using comparator function with _.sort() method
arr.sort(comp);

console.log("Sorted Array :", arr)
```

**输出:**

```
Sorted Array : [ 1, 2, 4, 8, 9 ]
```

**示例 2:** 使用比较器功能进行反向排序。

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var gfgFun = function(x, y) { 
    // Returns -1, 0 or 1
    return x >= y; 
};

// Array 
var arr = [4, 8, 2, 9, 1];

var comp = _.comparator(gfgFun);
// Using comparator function with _.sort() method
arr.sort(comp);

console.log("Sorted Array :", arr)
```

**输出:**

```
Sorted Array : [ 9, 8, 4, 2, 1 ]
```