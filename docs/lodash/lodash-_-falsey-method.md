# 洛达什 _。假()法

> 原文:[https://www.geeksforgeeks.org/lodash-_-falsey-method/](https://www.geeksforgeeks.org/lodash-_-falsey-method/)

**洛达什 _。false()方法**检查给定值是否为 false，并返回相应的布尔值。假值在布尔上下文中意味着假。

**语法:**

```
_.falsey( value );

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **值:**要检查给定值的假值。

**返回值:**如果给定值为假，则该方法返回布尔值 true，否则返回 false。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 lodash-contrib** 来安装 Lodash.js contrib 库。

**例 1:**

## java 描述语言

```
// Defining underscore lodash variable 
var _ = require('lodash-contrib'); 

var bool = _.falsey(false);

console.log("Given Value is Falsey : ", bool);
```

**输出:**

```
Given Value is Falsey : true

```

**例 2:**

## java 描述语言

```
// Defining underscore lodash variable 
var _ = require('lodash-contrib'); 

var bool = _.falsey(10);

console.log("Given Value is Falsey : ", bool);
```

**输出:**

```
Given Value is Falsey : false

```

**例 3:**

## java 描述语言

```
// Defining underscore lodash variable 
var _ = require('lodash-contrib'); 

var bool = _.falsey([ 1, 2, 3 ]);
console.log("Given Value is Falsey : ", bool);

var bool = _.falsey({});
console.log("Given Value is Falsey : ", bool);
```

**输出:**

```
Given Value is Falsey : false
Given Value is Falsey : false

```

**例 4:**

## java 描述语言

```
// Defining underscore lodash variable 
var _ = require('lodash-contrib'); 

var bool = _.falsey(false);
console.log("Given Value is Falsey : ", bool);

var bool = _.falsey("false");
console.log("Given Value is Falsey : ", bool);
```

**输出:**

```
Given Value is Falsey : true
Given Value is Falsey : false

```