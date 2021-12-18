# JavaScript | Uint8Array.from()方法

> 原文:[https://www . geesforgeks . org/JavaScript-uint 8 array-from-method/](https://www.geeksforgeeks.org/javascript-uint8array-from-method/)

**Uint8Array 数组**代表一个 8 位无符号整数数组。默认情况下，Uint8Array 的内容被初始化为 0。

**Uint8Array.from()方法**用于从类似数组或可迭代的对象创建新的 Uint8Array。因此，当您想要转换一个类似数组或可迭代的对象时，您可以使用这个函数，方法是将对象作为一个参数传递给这个函数，如果需要的话，还可以传递 map 函数和 map 函数使用的值。

**语法:**

```
Uint8Array.from( source, mapFn, thisArg )
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **来源:**此参数包含一个类似数组或可迭代的对象，用于转换为 Uint8Array 对象。
*   **mapFn:** 它是一个可选参数，是在 Uint8Array 数组的每个元素上调用的 Map 函数。
*   **该参数:**是一个可选参数，用于存储执行 mapFn 时的值。

**返回值:**这个方法返回一个新的 Uint8Array 实例。

下面的例子说明了在 JavaScript 中 Uint8Array.from()方法的工作原理:

**程序 1:**

```
<script>

// Create a Uint8Array from a string like structure
var  array = Uint8Array.from('45465768654323456');

// Print the result
document.write(array);
</script>
```

**输出:**

```
4, 5, 4, 6, 5, 7, 6, 8, 6, 5, 4, 3, 2, 3, 4, 5, 6
```

**程序二:**

```
<script>

// Create a Uint8Array from a array by adding
// 3 to each number using function
var  array = Uint8Array.from([1, 2, 3, 4, 5, 6], z => z+3);

// Print the result
document.write(array);
</script>
```

**输出:**

```
4, 5, 6, 7, 8, 9
```

**参考文献:**[https://developer . Mozilla . org/en-US/docs/Web/JavaScript/Reference/Global _ Objects/TypedArray/from](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/from)