# JavaScript | uint 8 clampedarray . from()方法

> 原文:[https://www . geesforgeks . org/JavaScript-uint 8 clampedarray-from-method/](https://www.geeksforgeeks.org/javascript-uint8clampedarray-from-method/)

**Uint8ClampedArray 数组**代表一个 8 位无符号整数数组，被箝位到 0-255。如果指定的值不在[0，255]范围内，将改为设置 0 或 255；如果指定的值不是整数，则将设置最接近的整数。默认情况下，Uint8ClampedArray 的内容被初始化为 0。

**Uint8ClampedArray . from()**方法用于从类似数组或可迭代的对象创建新的 uint 8 clampedarray。因此，当您想要将类似数组或可迭代的对象转换为 Uint8ClampedArray 时，您可以使用此函数，方法是将对象作为参数传递给此函数，如果需要，还可以传递 map 函数和 map 函数使用的值。

**语法:**

```
Uint8ClampedArray.from( source, mapFn, thisArg )

```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **来源**:这个参数是一个类似数组或者可迭代的对象，用来转换成 Uint8ClampedArray 对象。
*   **mapFn** :是一个可选参数，它是在 Uint8ClampedArray 数组的每个元素上调用的 Map 函数。
*   **此参数**:此参数是可选的，是执行 mapFn 时用作此参数的值。

**返回值**:这个方法返回一个新的 Uint8ClampedArray 实例。

下面的例子说明了在 JavaScript 中 Uint8ClampedArray.from()方法的工作原理:

**程序一:**

## Javascript

```
<script>

// Create a Uint8ClampedArray from
// a string like structure
var  array = Uint8ClampedArray.from('54323423');

// Display the result
document.write(array);
</script>
```

**输出:**

```
5, 4, 3, 2, 3, 4, 2, 3
```

**程序二:**

## JavaScript

```
<script>

// Create a Uint8ClampedArray from 
// an array by adding 32 to each
// number using function
var  array = Uint8ClampedArray.from(
    [229, 213, 200, 201, 204], z => z  + 32);

// Display the result
document.write(array);
</script>
```

**输出:**

```
255, 245, 232, 233, 236
```

**参考:**[https://developer . Mozilla . org/en-US/docs/Web/JavaScript/Reference/Global _ Objects/TypedArray/from](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/from)