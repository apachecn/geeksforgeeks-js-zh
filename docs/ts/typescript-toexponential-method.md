# TypeScript | toExponential()方法

> 原文:[https://www . geesforgeks . org/typescript-to exponential-method/](https://www.geeksforgeeks.org/typescript-toexponential-method/)

TypeScript 中的 **toExponential()方法**用于将一个数转换为它的指数形式。此方法根据给定的参数返回一个字符串，该字符串以指数表示法表示给定的 number 对象。

**语法:**

```
number.toExponential( [fractionDigits] )
```

**参数:**该方法接受一个参数，如上所述，如下所述:

*   **Score:** It is an integer value that specifies the number of digits after the decimal point. This is an optional parameter.

**返回值:**TypeScript 中的 **toExponential()** 方法返回一个字符串，该字符串以指数记数法表示数字对象，小数点前有一位数字。

以下示例说明了 TypeScript 中**到 Exponential()** 方法的工作原理:

**例 1:**

## 排版脚本

```
// Define a number to find the
// exponential notation
var num1 = 2762.30

// Find the exponential value
var val = num1.toExponential();

// Display the value
console.log(val)
```

**输出:**

```
2.7623e+3
```

**例 2:**

## 排版脚本

```
// Define a number to find the
// exponential notation
var num2 = 23456

// Find the exponential value
// with two digits after the
// decimal point
var val = num2.toExponential(2);

// Display the value
console.log(val)
```

**输出:**

```
2.34e+4
```