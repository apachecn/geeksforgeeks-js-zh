# 洛达什 _。流程()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-flow-method/](https://www.geeksforgeeks.org/lodash-_-flow-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。flow()** **方法**用于生成一个新的复合函数，该函数返回调用所提供函数的结果，该结果与所生成函数的*绑定。每个连续的调用都被提供前一个调用的返回值。*

***语法:***

```
*_.flow( funcs )*
```

***参数:**该方法接受如上所述的单个参数，如下所述:*

*   ***功能:**该参数保存要调用的功能。这是一个可选参数。*

***返回值:**该方法返回新的复合函数。*

***例 1:***

## *Javascript*

```
*// Requiring the lodash library 
const _ = require("lodash"); 

// Function to calculate the
// Cube of a number
function cube(number) {
  return number * number * number;
}

// Using the _.flow() method 
var multiplycube = _.flow([_.multiply, cube]);

// Return the output
console.log(multiplycube(2, 3));*
```

***输出:***

```
*216*
```

***例 2:***

## *【JavaScript】*

```
*// Requiring the lodash library 
const _ = require("lodash"); 

// Function to calculate the
// double value of a number
function doubled(number) {
  return number * 2;
}

// Using the _.flow() method 
var adddoubled = _.flow([_.add, doubled]);

// Return the output
console.log(adddoubled(6, 8));*
```

***输出:***

```
*28*
```