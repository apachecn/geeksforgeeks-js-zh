# 类型脚本| toLocaleString()函数

> 原文:[https://www . geesforgeks . org/typescript-tolocalesting-function/](https://www.geeksforgeeks.org/typescript-tolocalestring-function/)

TypeScript 中的 **toLocaleString()** 方法是使用环境的区域设置将数字转换为数字的本地特定表示。

**语法:**

```
number.toLocaleString()
```

**返回值:**TypeScript 中的 **toLocaleString()** 方法返回一个人类可读的字符串，该字符串使用环境的区域设置表示数字。

下面的例子说明了在 TypeScript 中 **toLocaleString()** 函数的工作原理:

**例 1:**

```
<script>

// toLocaleString() method
var num = new Number(432.3456);
console.log(num.toLocaleString());
</script>
```

**输出:**

```
432.3456

```

**例 2:**

```
<script>

// toLocaleString() method
let Number_1 : number = 23415.456;
console.log("Number Method: toLocaleString()");

// returns in US English
console.log(Number_1.toLocaleString()); 
</script>
```

**输出:**

```
Number Method: toLocaleString()
23, 415.456

```