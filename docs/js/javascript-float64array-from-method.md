# JavaScript | float 64 array . from()方法

> 原文:[https://www . geesforgeks . org/JavaScript-float 64 array-from-method/](https://www.geeksforgeeks.org/javascript-float64array-from-method/)

**Float64Array** 以平台字节顺序表示 64 位浮点数的数组。默认情况下，Float64Array 的内容用 0 初始化。
**Float64Array.from()方法**用于从类似数组或可迭代的对象创建一个新的 Float64Array。所以，当你想把一个类似数组或可迭代的对象转换成 Float64Array 时，你可以使用这个函数，把这个对象作为一个参数传递给这个函数，如果需要的话，还可以传递 map 函数和 map 函数的值。

**语法:**

```
Float64Array.from( source, mapFn, thisArg )
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **来源:**此参数保存一个类似数组或可迭代的对象，用于转换为 Float64Array 对象。
*   **mapFn:** 这个参数是可选的，它保存着 Map 函数来调用 Float64Array 数组的每个元素。
*   **此参数:**此参数是可选的，它保存在执行 mapFn 时用作此参数的值。

**返回值:**这个方法返回一个新的 Float64Array 实例。
以下示例说明了 JavaScript 中 Float64Array.from()函数的工作方式:
**示例 1:**

## java 描述语言

```
<script>

// Create a Float64Array from a string like structure
var  array = Float64Array.from('12345324354342354245342');

// Print the result
document.write(array);
</script>
```

**输出:**

```
1, 2, 3, 4, 5, 3, 2, 4, 3, 5, 4, 3, 4, 2, 3, 5, 4, 2, 4, 5, 3, 4, 2
```

**例 2:**

## java 描述语言

```
<script>

// Create a Float64Array from an array by
// multiplying 3999.99 to each number
// using function
var  array = Float64Array.from(
    [432.3343, 13243.3243123, 1324232132.24551],
    z => z  * 3999.99
);

// Print the result
document.write(array);
</script>
```

**输出:**

```
1729332.8766569998, 52973164.81595687, 5296915286660.718
```

**参考:**[https://developer . Mozilla . org/en-US/docs/Web/JavaScript/Reference/Global _ Objects/TypedArray/from](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/from)