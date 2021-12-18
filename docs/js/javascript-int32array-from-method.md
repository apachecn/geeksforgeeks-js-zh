# JavaScript | Int32Array.from()方法

> 原文:[https://www . geesforgeks . org/JavaScript-int 32 array-from-method/](https://www.geeksforgeeks.org/javascript-int32array-from-method/)

**Int32Array 数组**表示平台字节顺序的二进制补码 32 位有符号整数数组。默认情况下，Int32Array 的内容用 0 初始化。

**Int32Array.from()方法**用于从类似数组或可迭代的对象创建新的 Int32Array。因此，当您想要将一个类似数组或可迭代的对象转换为 Int32Array 时，您可以使用这个函数，方法是将该对象作为一个参数传递给这个函数，如果需要的话，还可以传递 map 函数和 map 函数使用的值。

**语法:**

```
Int32Array.from(source, mapFn, thisArg)

```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **来源**:这个参数是一个类似数组或者可迭代的对象，用来转换成 Int32Array 对象。
*   **mapFn** :这个参数是一个可选参数，是在 Int32Array 数组的每个元素上调用的 Map 函数。
*   **此参数**:此参数是一个可选参数，是执行 mapFn 时用作此参数的值。

**返回值**:这个方法返回一个新的 Int32Array 实例。

下面的例子说明了在 JavaScript 中 Int32Array.from()方法的工作原理:

**程序一:**

## JavaScript

```
<script>
// Create an Int32Array array from a
// string like structure
var  array = Int32Array.from('765432345');

// Print the result
document.write(array);
</script>
```

**输出:**

```
7, 6, 5, 4, 3, 2, 3, 4, 5
```

**程序二:**

## JavaScript

```
<script>
// Create an Int32Array array by converting
// numbers 32 times the actual number
var  array = Int32Array.from([434, 4323,
        43234, 433, 434, 343], z => z * 32 );

// Print the result
document.write(array);
</script>
```

**输出:**

```
13888, 138336, 1383488, 13856, 13888, 10976
```

**参考:**[https://developer . Mozilla . org/en-US/docs/Web/JavaScript/Reference/Global _ Objects/TypedArray/from](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/from)