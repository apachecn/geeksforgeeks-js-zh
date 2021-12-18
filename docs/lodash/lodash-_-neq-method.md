# 洛达什 _。neq()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-neq-method/](https://www.geeksforgeeks.org/lodash-_-neq-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。neq()方法**使用松散不等式(！=)并相应地返回一个布尔值。

**语法:**

```
_.neq( val1, val2, ..., valn )
```

**参数:**该方法取可变数量的值对其进行运算。

**返回值:**这个方法返回一个布尔值。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash contrib 库。可以使用 **npm 安装 Lodash-contrib–保存**来安装 Lodash contrib 库。

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Using the _.neq() method
var neq = _.neq( 3, 1 ); 

console.log(
  "Each arguments are not equal " +
  "to previous one :", neq
);
```

**输出:**

```
Each arguments are not equal to previous one : true
```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Using the _.neq() method
var neq = _.neq( 8, 8 );

console.log(
  "Each arguments are not equal " +
  "to previous one :", neq
);
```

**输出:**

```
Each arguments are not equal to previous one : false
```

**例 3:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Using the _.neq() method
var neq = _.neq( 8, 6, 4, 12 ); 

console.log(
  "Each arguments are not equal " +
  "to previous one :", neq
);
```

**输出:**

```
Each arguments are not equal to previous one : true
```

**例 4:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Using the _.neq() method
var neq = _.neq( 8, 8, 8, 8 );

console.log(
  "Each arguments are not equal " +
  "to previous one :", neq
);
```

**输出:**

```
Each arguments are not equal to previous one : false
```