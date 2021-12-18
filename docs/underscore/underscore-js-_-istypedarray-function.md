# 下划线. js _。isTypedArray()函数

> 原文:[https://www . geesforgeks . org/下划线-js-_-istypedray-function/](https://www.geeksforgeeks.org/underscore-js-_-istypedarray-function/)

**下划线. js** 是一个 JavaScript 库，它提供了许多有用的函数，这些函数在很大程度上有助于编程，比如映射、过滤、调用等，甚至不使用任何内置对象。

**_。isTypedArray()函数**是 JavaScript 的下划线. js 库中的一个内置函数，用于检查所述对象是否是*类型的函数*。

**语法:**

```
_.isTypedArray(object)
```

**参数:**它接受以下指定的单个参数:

*   **对象:**是陈述的对象。

**返回值:**如果所述对象是*类型的，则该方法返回真，否则返回假。*

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.11.0/underscore-min.js">
    </script>
</head>

<body>
    <script>
        console.log(_.isTypedArray(new Int8Array(7, 6)));
    </script>
</body>

</html>
```

**输出:**

```
true
```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.11.0/underscore-min.js">
    </script>
</head>

<body>
    <script>
        console.log(_.isTypedArray("geeksforgeeks.."));
    </script>
</body>

</html>
```

**输出:**

```
false
```

**参考:**T2】https://underscorejs.org/#isTypedArray