# 洛达什 _。isDecreasing()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isdecreasing-method/](https://www.geeksforgeeks.org/lodash-_-isdecreasing-method/)

**_。方法检查参数是否是单调递减的值，或者每个参数是否小于前一个参数。**

**语法:**

```
_.isDecreasing(val1,val2,...,valn);

```

**参数:**该方法 n 个值检查递减顺序。

**返回值:**该方法返回一个布尔值(如果给定值在减少，则返回**真**，否则返回**假**)。

**注意:**要执行以下示例，您必须使用此命令提示符安装 **lodash-contrib** 库，并执行以下命令。

```
npm install lodash-contrib

```

以下示例说明了 Lodash _。JavaScript 中的 isDecreasing()方法:

**例 1:**

## Javascript

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Checking 
console.log("The Value is Decreasing : " 
            +_.isDecreasing(5,4,3,2,1));
```

**输出:**

```
The Value is Decreasing : true

```

**例二:**

## Javascript

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Checking 
console.log("The Value is Decreasing : " 
             +_.isDecreasing(3,2,1,2));
```

**输出:**

```
The Value is Decreasing : false

```