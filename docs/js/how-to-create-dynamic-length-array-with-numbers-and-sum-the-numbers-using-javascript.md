# 如何用数字创建动态长度数组，并用 JavaScript 对数字求和？

> 原文:[https://www . geeksforgeeks . org/如何使用 javascript 创建带有数字和数字总和的动态长度数组/](https://www.geeksforgeeks.org/how-to-create-dynamic-length-array-with-numbers-and-sum-the-numbers-using-javascript/)

在 JavaScript 中， [数组](https://www.geeksforgeeks.org/arrays-in-javascript/) 是用于存储不同元素的单个变量。当我们想要存储元素列表并通过单个变量访问它们时，通常会用到它。与大多数语言中数组是对多个变量的引用不同，在 JavaScript 中，数组是存储多个元素的单个变量。

JavaScript 数组本质上是**动态的**意思是，数组的长度可以在运行时修改(必要时)。可以在声明数组后指定数组长度，如下例所示。

**例:**

## Javascript

```
// Declare an array of undefined size
var arr = [];

// Set array length to 10
arr.length = 10;

// Print the length to console
console.log(arr);
```