# 类型脚本|数组拼接()方法

> 原文:[https://www . geesforgeks . org/typescript-array-splice-method/](https://www.geeksforgeeks.org/typescript-array-splice-method/)

**Array.splice()** 是一个内置的 TypeScript 函数，用于更改数组的内容，在删除旧元素的同时添加新元素。
**语法:**

```
array.splice(index, howMany, [element1][, ..., elementN]); 
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **索引:**该参数是开始改变数组的索引。
*   **多少:**此参数是表示要移除的旧数组元素数量的整数。
*   **element1、…、elementN :** 此参数是要添加到数组中的元素。

**返回值:**该方法返回提取的数组。
以下示例说明了 TypeScriptJS 中的 Array splice()方法:
**示例 1:**

## Java Script 语言

```
<script>
    // Driver code
    var arr = [ 11, 89, 23, 7, 98 ]; 

    // use of splice() method 
    var removed = arr.splice(2, 0, 11);

    // printing
    console.log(removed);
</script>
```