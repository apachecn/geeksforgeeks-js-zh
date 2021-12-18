# JavaScript | Uint32Array from()方法

> 原文:[https://www . geesforgeks . org/JavaScript-uint 32 array-from-method/](https://www.geeksforgeeks.org/javascript-uint32array-from-method/)

Uint32Array 数组表示平台字节顺序的 32 位无符号整数数组。默认情况下，Uint32Array 的内容被初始化为 0。
**from()** 功能的 **Uint32Array** 用来从一个类似数组或可迭代的对象创建一个新的 Uint32Array。因此，当您想要转换一个类似数组或可迭代的对象时，您可以使用这个函数，方法是将对象作为一个参数传递给这个函数，如果需要的话，还可以传递 map 函数和 map 函数使用的值。
**语法:**

```
Uint32Array.from(source[, mapFn[, thisArg]])
```

**参数:**该方法接受以下指定的三个参数:

1.  **来源**:这个参数是一个类似数组或者可迭代的对象，用来转换成 Uint32Array 对象。
2.  **mapFn** :这个参数是可选的，是在 Uint32Array 数组的每个元素上调用的 Map 函数。
3.  **此参数**:此参数是可选的，是执行 mapFn 时用作此参数的值。

**返回值:**这个方法返回一个新的 Uint32Array 实例。
JavaScript 程序来说明 from()函数的工作:
**程序 1:**

## java 描述语言

```
<script>
    //create a Uint32Array from a string like structure
    var array = Uint32Array.from('987654321234567');

    //print the result
    document.write(array);
</script>
```

**输出:**

```
9, 8, 7, 6, 5, 4, 3, 2, 1, 2, 3, 4, 5, 6, 7
```

**节目 2:**

## java 描述语言

```
<script>
    //create a Uint32Array from a array by
    //dividing by 32 to each number using function
    var array = Uint32Array.from([543234, 432345, 5432123, 43234,
        23432, 5432345, 432345, 23432
    ], z => z / 32);

    //print the result
    document.write(array);
</script>
```

**输出:**

```
16976, 13510, 169753, 1351, 732, 169760, 13510, 732
```

**参考文献:**
[https://developer . Mozilla . org/en-US/docs/Web/JavaScript/Reference/Global _ Objects/TypedArray/from #](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/from#)