# 类型脚本|数组 forEach()方法

> 原文:[https://www . geesforgeks . org/typescript-array-foreach-method/](https://www.geeksforgeeks.org/typescript-array-foreach-method/)

**Array.forEach()** 是一个内置的 TypeScript 函数，用于为数组中的每个元素调用一个函数。
**语法:**

```
array.forEach(callback[, thisObject])
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **回调:**该参数是对每个元素进行测试的函数。
*   **thisObject :** 此参数是执行回调时用作此的对象。

**返回值:**该方法返回创建的数组。
下面的例子说明了打字稿中的**数组 forEach()** 方法。

**例 1:**

## Java Script 语言

```
<script>
    // Driver code
    var arr = [ 11, 89, 23, 7, 98 ]; 

    // printing eah element
    arr.forEach(function (value) {
        console.log(value);
    });
</script>
```

**输出:**

```
11
89
23
7
98

```

**例 2:**

## Java Script 语言

```
<script>
    // Driver code
    var arr = [ 1, 2, 3, 4, 5 ]; 

    // printing square of  element
    arr.forEach(function (value) {
        console.log(value * value);
    });
</script>
```

**输出:**

```
1
4
9
16
25

```