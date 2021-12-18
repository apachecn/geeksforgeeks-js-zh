# 类型脚本|数组 unshift()方法

> 原文:[https://www . geesforgeks . org/typescript-array-unshift-method/](https://www.geeksforgeeks.org/typescript-array-unshift-method/)

**Array.unshift()** 是一个内置的 TypeScript 函数，用于将一个或多个元素添加到数组的开头，并返回数组的新长度。
**语法:**

```
array.unshift( element1, ..., elementN )
```

**参数:**该方法接受 n 个相似元素。

*   **element1，…，elementN :** 这个参数是要添加到数组前面的元素。

**返回值:**这个方法返回新数组的长度。
下面的示例说明了打字稿中的**字符串 unshift()** 方法:

**例 1:**

## Java Script 语言

```
<script>
    // Driver code
    var arr = [ 11, 89, 23, 7, 98 ]; 

    // use of unshift() method 
    var tring= arr.unshift(11);

    // printing
    console.log( tring);
</script>
```

**输出:**

```
6

```

**例 2:**

## Java Script 语言

```
<script>
    // Driver code
    var arr = ["G", "e", "e", "k", "s", "f", "o",
               "r", "g", "e", "e", "k", "s"]; 
    var val;

    // use of unshift() method 
    val = arr.unshift("f");
    console.log( val );
    console.log( arr );
</script>
```

**输出:**

```
14
["f","G","e","e","k","s","f","o","r","g","e","e","k","s"]

```