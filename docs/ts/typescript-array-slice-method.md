# 类型脚本|数组切片()方法

> 原文:[https://www . geesforgeks . org/typescript-array-slice-method/](https://www.geeksforgeeks.org/typescript-array-slice-method/)

**Array.slice()** 是一个内置的 TypeScript 函数，用于提取数组的一部分并返回一个新的数组。
**语法:**

```
 array.slice( begin [,end] ); 
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **开始:**此参数是从零开始提取的索引。
*   **结束:**此参数是结束提取的从零开始的索引。

**返回值:**该方法返回提取的数组。
以下示例说明了 TypeScriptJS 中的**数组切片()**方法:
**示例 1:**

## 以打字打的文件

```
// Driver code
var arr = [ 11, 89, 23, 7, 98 ]; 

// use of slice() method 
var val = arr.slice(2, 4);

// printing
console.log( val );
```