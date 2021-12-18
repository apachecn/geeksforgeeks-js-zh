# JavaScript | Unit16Array.from()方法

> 原文:[https://www . geesforgeks . org/JavaScript-unit 16 array-from-method/](https://www.geeksforgeeks.org/javascript-unit16array-from-method/)

Uint16Array 数组表示平台字节顺序的 16 位无符号整数数组。默认情况下，Uint16Array 的内容被初始化为 0。
**Uint16Array . from()函数**用于从类似数组或可迭代的对象创建新的 uint 16 array。因此，当您想要转换一个类似数组或可迭代的对象时，您可以使用这个函数，方法是将对象作为一个参数传递给这个函数，如果需要的话，还可以传递 map 函数和 map 函数使用的值。

**语法:**

```
Uint16Array.from( source, mapFn, thisArg )
```

**参数:**该方法接受三个参数，如上所述，如下所述。

*   **来源:**此参数是一个类似数组或可迭代的对象，用于转换为 Uint16Array 对象。
*   **mapFn:** 这个参数是可选的，它是在 Uint16Array 数组的每个元素上调用的 Map 函数。
*   **此参数:**此参数是可选的，它是执行 mapFn 时用作此参数的值。

**返回值:**这个方法返回一个新的 Uint16Array 实例。

以下示例说明了 JavaScript 中的**单元 16Array.from()方法**:

**程序 1:**

```
<script>

// Create a Uint16Array from a string
// like structure
var  array = Uint16Array.from('543234543');

// Print the result
document.write(array);
</script>
```

**输出:**

```
5, 4, 3, 2, 3, 4, 5, 4, 3
```

**程序 2:**

```
<script>

// Create a Uint16Array from a array 
// multiplying 3 to each number
// using function
var  array = Uint16Array.from([32, 
       53, 122, 434, 213], z => z*3);

// Print the result
document.write(array);
</script>
```

**输出:**

```
96, 159, 366, 1302, 639
```

**参考文献:**[https://developer . Mozilla . org/en-US/docs/Web/JavaScript/Reference/Global _ Objects/TypedArray/from #](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/from#)