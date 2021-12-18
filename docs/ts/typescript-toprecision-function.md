# 打字稿|精确()功能

> 原文:[https://www . geesforgeks . org/typescript-to precision-function/](https://www.geeksforgeeks.org/typescript-toprecision-function/)

TypeScript 中的 **toPrecision()** 方法用于将指数或定点形式的字符串表示返回到指定的精度。

**语法:**

```
number.toPrecision( [ precision ] )

```

**参数:**表示指定有效位数的整数值。

**返回值:**Typescript 中的 **toPrecision()** 方法返回一个字符串，该字符串以定点或指数表示法表示四舍五入到有效数字的数字。

以下示例说明了 TypeScript 中 **toPrecision()** 函数的工作原理:

**例 1:**

```
<script>

// toPrecision() method
var num = new Number(6.218956); 
console.log(num.toPrecision()); 
console.log(num.toPrecision(4)); 
console.log(num.toPrecision(3));
</script>
```

**输出:**

```
6.218956 
6.2189 
6.21

```

**例 2:**

```
<script>

// toPrecision() method
let myNumber: number = 32.5779; 
console.log("Number Method: toPrecision()");  
console.log(myNumber.toPrecision(1));   
console.log(myNumber.toPrecision(3));  
</script>
```

**输出:**

```
Number Method: toPrecision()
3e+1
32.6

```