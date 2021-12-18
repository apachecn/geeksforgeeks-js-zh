# 洛达什 _。neg()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-neg-method/](https://www.geeksforgeeks.org/lodash-_-neg-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。neg()方法**用于返回一个与给定数字符号值相反的新数字。

**语法:**

```
_.neg( value )

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**是用这种方法求反的数。

**返回值:**该方法返回一个与给定数字符号值相反的新数字。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash contrib 库。可以使用 **npm 安装 Lodash-contrib–保存**来安装 Lodash contrib 库。

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Using the _.neg() method
var n  = _.neg( -1 ); 

console.log(
  "Opposite sign value number is :", n
);
```

**输出:**

```
Opposite sign value number is : 1

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Using the _.neg() method
var n  = _.neg( 1 ); 

console.log(
  "Opposite sign value number is :", n
);
```

**输出:**

```
Opposite sign value number is : -1

```

**例 3:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Using the _.neg() method
var n  = _.neg( 60 ); 

console.log(
  "Opposite sign value number is :", n
);
```

**输出:**

```
Opposite sign value number is : -60

```

**例 4:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Using the _.neg() method
var n  = _.neg( -50 ); 

console.log(
  "Opposite sign value number is :", n
);
```

**输出:**

```
Opposite sign value number is : 50

```