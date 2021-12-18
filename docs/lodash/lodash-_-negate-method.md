# 洛达什 _。否定()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-negate-method/](https://www.geeksforgeeks.org/lodash-_-negate-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。否定()** **方法**用于创建一个否定给定*谓词*函数结果的函数。

**语法:**

```
_.negate( predicate )

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **谓词:**此参数保存要求反的谓词函数。

**返回值:**该方法返回新的求反函数。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Function to check the number
// is divisible by 5 or not
function number(n) {
  return n % 5 == 0;
}

// Using the _.negate() method  
console.log(
  _.filter([4, 6, 10, 15, 18], 
  _.negate(number))
);
```

**输出:**

```
[4, 6, 18]

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Function to check the
// number is odd or not
function isOdd(n) {
  return n % 2 != 0;
}

// Using the _.negate() method  
console.log(
  _.filter([2, 4, 7, 12, 16, 19],
  _.negate(isOdd))
);
```

**输出:**

```
[2, 4, 12, 16]

```