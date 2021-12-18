# 排版| toFixed()功能

> 原文:[https://www.geeksforgeeks.org/typescript-tofixed-function/](https://www.geeksforgeeks.org/typescript-tofixed-function/)

[](https://www.geeksforgeeks.org/hello-world-in-typescript-language/)**中的 **toFixed(** ) **功能**用于使用定点符号格式化数字。它可以用来格式化小数点右边有特定位数的数字。**

****语法:****

```
number.toFixed( [digits] ); 
```

****参数:**该函数接受一个参数值- **位数**–小数点后出现的位数。**

****返回值:**TypeScript 中的 **toFixed()** 方法返回一个数字的字符串表示形式，它不使用指数表示法，并且在小数点后有精确的位数。**

**以下示例说明了 **toFixed()** 函数在 TypeScript 中的工作:
**示例 1:****

## **java 描述语言**

```
var num = 358.429 
console.log("num.toFixed() is "+num.toFixed()) 
console.log("num.toFixed(2) is "+num.toFixed(2))
```

****输出:****

```
num.toFixed() is 358 
num.toFixed(2) is 358.42 
```

****例 2:****

## **java 描述语言**

```
var num1 = 526.123 
console.log("num1.toFixed() is "+num1.toFixed()) 
console.log("num1.toFixed(4) is "+num1.toFixed(4)) 
console.log("num1.toFixed(7) is "+num1.toFixed(7))
```

****输出:****

```
num1.toFixed() is 526 
num1.toFixed(4) is 526.1230
num1.toFixed(7) is 526.1230000 
```