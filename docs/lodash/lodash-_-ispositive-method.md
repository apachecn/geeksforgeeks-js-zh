# 洛达什 _。isPositive()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-ispositive-method/](https://www.geeksforgeeks.org/lodash-_-ispositive-method/)

**洛达什 _。isPositive()方法**检查给定值是否为正，并返回相应的布尔值。

**语法:**

```
_.isPositive(value);
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**要检查正值的给定值。

**返回值:**如果给定值为正，则该方法返回布尔值 true，否则返回 false。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用以下命令安装 Lodash.js contrib 库:

```
npm install lodash-contrib
```

**例 1:**

```
// Defining underscore lodash variable 
var _ = require('lodash-contrib'); 

// Checking for _.isPositive() method 
console.log("The Value is Positive : " + _.isPositive(20));
```

**输出:**

```
The Value is Positive : true
```

**例 2:**

```
// Defining underscore lodash variable 
var _ = require('lodash-contrib'); 

// Checking for _.isPositive() method 
console.log("The Value is Positive : " + _.isPositive(-1000));

console.log("The Value is Positive : " + _.isPositive("100"));
```

**输出:**

```
The Value is Positive : false
The Value is Positive : true
```

**例 3:**

```
// Defining underscore lodash variable 
var _ = require('lodash-contrib'); 

// Checking for _.isPositive() method 
console.log("The Value is Positive : " + _.isPositive(true));

console.log("The Value is Positive : " + _.isPositive([10, 20]));
```

**输出:**

```
The Value is Positive : true
The Value is Positive : false
```