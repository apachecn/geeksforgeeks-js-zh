# ES6 中使用的编号方法有哪些？

> 原文:[https://www . geeksforgeeks . org/es6 中使用的方法数量是多少/](https://www.geeksforgeeks.org/what-are-the-number-methods-used-in-es6/)

数字是 JavaScript 中的基本数据类型之一。对于不同的数字，JavaScript 没有任何特定的数据类型(如 int、float、long 等)。它只有一种数据类型，即数字。它可以写有或没有小数。它们基本上是 64 位双精度浮点值。

ES6 中使用了 6 种不同的编号方法:

**1。 [Number.isNaN()](https://www.geeksforgeeks.org/number-isnan-javascript/) :** 用于检查通过值是否为 **NaN** 。如果是*号*或*串*或*未定义，*会给**假。**
**例:**

## java 描述语言

```
<script>
    console.log(Number.isNaN(NaN)); // true
    console.log(Number.isNaN(0/0)); // true
    console.log(Number.isNaN(10));  //  false
    console.log(Number.isNaN("Sarthak")); // false
    console.log(Number.isNaN("NaN")); // false
</script>
```