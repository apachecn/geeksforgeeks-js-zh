# 洛达什 _。方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isindexed-method/](https://www.geeksforgeeks.org/lodash-_-isindexed-method/)

**洛达什 _。isIndexed()方法**检查给定值是否可以认为是“Indexed”，并返回相应的布尔值。索引值是接受索引来访问其元素的值。

**语法:**

```
_.isIndexed( value );

```

**参数:**该方法取上述单参数，描述如下:

*   **值:**要检查索引值的给定值。

**返回值:**如果给定值是 Indexed，则该方法返回布尔值 true，否则返回 false。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 lodash-contrib** 来安装 Lodash.js contrib 库。

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Checking for index value
console.log("The Value is Indexed : " 
    + _.isIndexed([1, 3, 5]));
```

**输出:**

```
The Value is Indexed : true

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Checking for index value
console.log("The Value is Indexed : " 
    + _.isIndexed({1:3, 2:3});
```

**输出:**

```
The Value is Indexed : false

```

**例 3:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Checking for index value
console.log("The Value is Indexed : " 
    + _.isIndexed("GeeksforGeeks"));
```

**输出:**

```
The Value is Indexed : true

```