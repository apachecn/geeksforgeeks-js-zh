# 洛达什 _。增加()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isincreasing-method/](https://www.geeksforgeeks.org/lodash-_-isincreasing-method/)

**洛达什 _。isIncreasing()方法**检查给定值是否单调递增(每个自变量都大于前一个自变量)。

**语法:**

```
_.isIncreasing(val1, val2, ..., valn);

```

**参数:**该方法取 n 个值检查递增顺序。

**返回值:**该方法返回一个布尔值(如果给定值为递增，则返回真，否则返回假)。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 lodash-contrib** 来安装 Lodash.js contrib 库。

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Check for increasing order
console.log("The Value is Increasing order : " 
    + _.isIncreasing(1, 2, 3, 4));
```

**输出:**

```
The Value is Increasing order : true

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Check for increasing order
console.log("The Value is Increasing : " 
    + _.isIncreasing(3, 2, 1, 2));
```

**输出:**

```
The Value is Increasing : false

```

**例 3:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Check for increasing order
console.log("The Value is Increasing : " 
    + _.isIncreasing('a', 'b'));

console.log("The Value is Increasing : " 
    + _.isIncreasing('c', 'b', 'a'));
```

**输出:**

```
The Value is Increasing : true
The Value is Increasing : false

```

**例 4:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Check for increasing order
console.log("The Value is Increasing : " 
    + _.isIncreasing("Geeks", "GFG"));

console.log("The Value is Increasing : " 
    + _.isIncreasing('g', 'G'));
```

**输出:**

```
The Value is Increasing : false
The Value is Increasing : false

```