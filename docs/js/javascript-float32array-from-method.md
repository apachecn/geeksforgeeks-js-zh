# JavaScript | float 32 array . from()方法

> 原文:[https://www . geesforgeks . org/JavaScript-float 32 array-from-method/](https://www.geeksforgeeks.org/javascript-float32array-from-method/)

Float32Array 数组以平台字节顺序表示 32 位浮点数的数组。默认情况下，Float32Array 的内容被初始化为 0。

**Float32Array.from()方法**用于从类似数组或可迭代的对象创建新的 Float32Array。因此，当您想要将一个数组类或可迭代对象转换为 Float32Array 时，您可以使用这个函数，方法是将该对象作为参数传递给这个函数，如果需要的话，还可以传递 map 函数和 map 函数使用的值。

**语法:**

```
Float32Array.from( source, mapFn, thisArg )
```

**参数:**该方法接受三个参数，如上所述，如下所述。

*   **来源:**此参数是一个类似数组或可迭代的对象，用于转换为 Float32Array 对象。
*   **mapFn:** 这个参数是可选的，它是一个 Map 函数，用来调用 Float32Array 数组的每个元素。
*   **此参数:**此参数是可选的，它是执行 mapFn 时用作此参数的值。

**返回值:**这个方法返回一个新的 Float32Array 实例。

以下示例说明了 JavaScript 中的 **Float32Array.from()方法**:

**节目 1:**

```
<script> 

// Create a Float32Array from a string like structure
var  array = Float32Array.from('7654312456754');

// Print the result
document.write(array);
</script>
```

**输出:**

```
7, 6, 5, 4, 3, 1, 2, 4, 5, 6, 7, 5, 4
```

**节目 2:**

```
<script>

// Create a Float32Array from an array by
// multiplying 33.32 to each number using
// function
var  array = Float32Array.from([5232.4242,
        3114.24551], z => z  * 33.32);

// Print the result
document.write(array);
</script>
```

**输出:**

```
174344.375, 103766.6640625
```

**参考文献:**[https://developer . Mozilla . org/en-US/docs/Web/JavaScript/Reference/Global _ Objects/TypedArray/from #](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/from#)