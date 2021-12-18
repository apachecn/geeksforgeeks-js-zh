# JavaScript | Int16Array from()方法

> 原文:[https://www . geesforgeks . org/JavaScript-int 16 array-from-method/](https://www.geeksforgeeks.org/javascript-int16array-from-method/)

Int16Array 数组表示 16 位有符号整数的二进制补码数组。默认情况下，Int16Array 的内容被初始化为 0。
来自 Int16Array 的()函数，用于从类似数组或可迭代的对象创建新的 Int16Array。因此，当您想要将类似数组或可迭代的对象转换为 Int16Array 时，您可以使用该函数，方法是将该对象作为参数传递给该函数，如果需要，还可以传递 map 函数和 map 函数所用的值。

**语法:**

```
Int16Array.from(source[, mapFn[, thisArg]])
```

**参数:**该方法接受以下指定的三个参数:

1.  **来源:**此参数是一个类似数组或可迭代的对象，用于转换为 Int16Array 对象。
2.  **mapFn:** 这个参数是可选的，它是在 Int16Array 数组的每个元素上调用的 Map 函数。
3.  **此参数:**此参数是可选的，是执行 mapFn 时用作此参数的值。

**返回值**:这个方法返回一个新的 Int16Array 实例。
JavaScript 程序说明 from()函数的工作原理:
**程序 1:**

## java 描述语言

```
<script>
    //create a Int16Array from a string like structure
    var array = Int16Array.from('654456543456');

    //print the result
    document.write(array);
</script>
```

**输出:**

```
6, 5, 4, 4, 5, 6, 5, 4, 3, 4, 5, 6
```

**程序 2:**

## java 描述语言

```
<script>
    //create a Int16Array from a array by converting numbers
    //twice the actual number
    var array = Int16Array.from([32, 43, 41, 34], z => z * 2);

    //print the result
    document.write(array);
</script>
```

**输出:**

```
64, 86, 82, 68
```

**参考文献:**
[https://developer . Mozilla . org/en-US/docs/Web/JavaScript/Reference/Global _ Objects/TypedArray/from #](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/from#)