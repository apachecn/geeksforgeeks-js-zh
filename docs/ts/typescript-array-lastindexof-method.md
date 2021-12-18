# 类型脚本|数组 lastIndexOf()方法

> 原文:[https://www . geesforgeks . org/typescript-array-last indexof-method/](https://www.geeksforgeeks.org/typescript-array-lastindexof-method/)

**Array.lastIndexOf()** 是一个内置的 [**TypeScript**](https://www.geeksforgeeks.org/hello-world-in-typescript-language/) 函数，用于获取数组中给定元素的最后一个索引。
**语法:**

```
array.lastIndexOf(searchElement[, fromIndex])
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **searchElement :** 此参数是要在数组中定位的元素。
*   **fromIndex :** 此参数是开始向后搜索的索引。

**返回值:**这个方法返回从最后一个找到的元素的索引。
以下示例说明了 TypeScript 中的**数组 lastIndexOf()** 方法。
**例 1:**

## Java Script 语言

```
<script>
    // Driver code
    var arr = [ 11, 89, 23, 7, 98 ]; 

    // use of lastIndexOf() method 
    var val = arr.lastIndexOf(7)

    // printing element
    console.log( val );
</script>
```