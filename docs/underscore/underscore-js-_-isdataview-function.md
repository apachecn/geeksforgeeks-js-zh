# 下划线. js _。isDataView()功能

> 原文:[https://www . geesforgeks . org/下划线-js-_-isdataview-function/](https://www.geeksforgeeks.org/underscore-js-_-isdataview-function/)

**下划线. js** 是一个 JavaScript 库，它提供了许多有用的函数，这些函数在很大程度上有助于编程，比如映射、过滤、调用等，甚至不使用任何内置对象。

**_。isDataView()函数**是 JavaScript 的下划线. js 库中的一个内置函数，用于检查所述对象是否是*数据视图*。

**语法:**

```
_.isDataView(object)
```

**参数:**它接受以下指定的单个参数:

*   **对象:**是陈述的对象。

**返回值:**如果所述对象是*数据视图*，则该方法返回真，否则返回假。

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
        var buff = new ArrayBuffer(11);

        console.log(_.isDataView(
            new DataView(buff, 3, 5)));
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
        console.log(_.isDataView("Geeks!"));
    </script>
</body>

</html>
```

**输出:**

```
false
```

**参考:**T2】https://underscorejs.org/#isDataView