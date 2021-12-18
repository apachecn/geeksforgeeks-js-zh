# JavaScript | Int8Array from()方法

> 原文:[https://www . geesforgeks . org/JavaScript-int 8 array-from-method/](https://www.geeksforgeeks.org/javascript-int8array-from-method/)

Int8Array 数组表示 8 位有符号整数的二进制补码数组。默认情况下，Int8Array 的内容被初始化为 0。来自用于从类似数组或可迭代对象创建新 Int8Array 的 Int8Array 的()函数。因此，当您想要将 arrayLike 或 iterable 对象转换为 Int8Array 时，您可以使用此函数，方法是将对象作为参数传递给此函数，如果需要，还可以传递 map 函数和 map 函数使用的值。
**语法:**

```
Int8Array.from(source[, mapFn[, thisArg]])
```

**参数:**该方法接受以下指定的三个参数-

1.  **来源**:这个参数是一个类似数组或者可迭代的对象，用来转换成 Int8Array 对象。
2.  **mapFn** :这个参数是可选的，是在 Int8Array 数组的每个元素上调用的 Map 函数。
3.  **此参数**:此参数是可选的，是执行 mapFn 时用作此参数的值。

**返回值**:这个方法返回一个新的 Int8Array 实例。
JavaScript 程序来说明 from()函数的工作:
**程序 1:**

## java 描述语言

```
<script>
    //create a Int8Array from a string like structure
    var array = Int8Array.from('876543456789');

    //print the result
    document.write(array);
</script>
```

**输出:**

```
8, 7, 6, 5, 4, 3, 4, 5, 6, 7, 8, 9
```

**节目 2:**

## java 描述语言

```
<script>
    //create a Int8Array from a array by
    //adding 1 to each number using function
    var array = Int8Array.from([9, 2, 1, 4, 3], z => z + 1);

    //print the result
    document.write(array);
</script>
```

**输出:**

```
10, 3, 2, 5, 4
```

**参考文献:**
[https://developer . Mozilla . org/en-US/docs/Web/JavaScript/Reference/Global _ Objects/TypedArray/from #](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/from#)