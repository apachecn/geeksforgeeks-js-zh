# JavaScript | symbol . isncatspreable 符号

> 原文:[https://www . geeksforgeeks . org/JavaScript-symbol-isncatspreable-symbol/](https://www.geeksforgeeks.org/javascript-symbol-isconcatspreadable-symbol/)

**符号是一个众所周知的符号，用于*配置在使用 Array.prototype.concat()方法时，给定对象是否应展平为其数组元素。*
**语法:**** 

```
Array[Symbol.isConcatSpreadable]
```

这里**数组**是要展平为其数组元素的数组对象。
**参数:**此符号不接受任何参数。
**返回值:**此符号不返回值。
JavaScript 代码展示这个函数的工作原理。
**示例-1:**

## java 描述语言

```
<script>
   // Creating some arrays
   const Array1 = [1, 2, 3];
   const Array2 = [4, 5, 6];

   // Calling concat() function
   let Array3 = Array1.concat(Array2);

   // Printing the concatenated array
   console.log(Array3);

   // Calling Symbol.isConcatSpreadable symbol
   Array2[Symbol.isConcatSpreadable] = false;
   Array3 = Array1.concat(Array2);

   // Printing the concatenated array
   // after calling of Symbol.isConcatSpreadable symbol
   console.log(Array3);
</script>
```

**输出:**

```
> Array [1, 2, 3, 4, 5, 6]
> Array [1, 2, 3, Array [4, 5, 6]]
```

**示例-2:**

## java 描述语言

```
<script>
   // Creating some arrays
   const Array1 = [1, 2, 3];
   const Array2 = [4, 5, 6];

   // Calling concat() function
   let Array3 = Array1.concat(Array2);

   // Printing the concatenated array
   console.log(Array3);

   // Calling Symbol.isConcatSpreadable symbol
   Array2[Symbol.isConcatSpreadable] = true;
   Array3 = Array1.concat(Array2);

   // Printing the concatenated array
   // after calling of Symbol.isConcatSpreadable symbol
   console.log(Array3);
</script>
```

**输出:**

```
> Array [1, 2, 3, 4, 5, 6]
> Array [1, 2, 3, 4, 5, 6]
```

**支持的浏览器:**

*   谷歌 Chrome 48 及以上
*   Firefox 48 及以上版本
*   边缘 15 及以上
*   歌剧 35 及以上
*   Apple Safari 10 及以上版本