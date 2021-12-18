# 类型脚本|数组 concat()方法

> 原文:[https://www . geesforgeks . org/typescript-array-concat-method/](https://www.geeksforgeeks.org/typescript-array-concat-method/)

**Array.concat()** 是一个内置的 [**TypeScript**](https://www.geeksforgeeks.org/hello-world-in-typescript-language/) 函数，用于将两个或多个数组合并在一起。
**语法:**

```
array.concat(value1, value2, ..., valueN)
```

**参数:**该方法如上所述多次接受单个参数，如下所述:

*   **值 N :** 这些参数是要连接的数组和/或值。

**返回值:**此方法返回新数组。
以下示例说明了 TypeScript 中的**数组 concat()** 方法
**示例 1:**

## Java Script 语言

```
<script>
    // Driver code
    var num1 = [11, 12, 13];
    var num2 = [14, 15, 16];
    var num3 = [17, 18, 19]; 

    // use of String concat() Method
    console.log(num1.concat(num2, num3)); 
</script>
```