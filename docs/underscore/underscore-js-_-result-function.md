# 下划线. js _。结果()函数

> 原文:[https://www . geesforgeks . org/下划线-js-_-结果-函数/](https://www.geeksforgeeks.org/underscore-js-_-result-function/)

**下划线. js** 是一个 JavaScript 库，它提供了很多有用的函数，在很大程度上有助于编程，比如映射、过滤、调用等，甚至不使用任何内置对象。

**_。result()函数**是 JavaScript 的下划线. js 库中的一个内置函数。这里，如果指定属性的指定值是一个函数，那么您应该将对象作为上下文来调用它，否则返回它。此外，如果声明了默认值，而属性参数未给出或未定义，则将返回默认值。

**注意:**如果所述的*默认值*是一个函数，那么其结果将作为输出返回。

**语法:**

```
_.result(object, property, [defaultValue])
```

**参数:**接受以下指定的三个参数:

*   **Object:** is the stated object.
*   **Attribute:** is the stated attribute.
*   **[default value]:** is the specified default value.

**返回值:**此方法返回命名属性的值。

**例 1:**

## Javascript

```
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
    </script>
</head>

<body>
    <script>
        var obj = { 
            CSportal: 'GeeksforGeeks', 
            gfg: function () { return 'Geeks!'; } 
        };

        // Calling result method with its parameters
        console.log(_.result(obj, 'CSportal'));
    </script>
</body>

</html>
```

**输出:**

```
GeeksforGeeks
```

**例二:**

## Javascript

```
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
    </script>
</head>

<body>
    <script>
        var obj = [1, 2, 4, 5];

        // Calling result method 
        // with its parameters
        console.log(_.result(obj, 9, 7));
        console.log(_.result(obj, 5));
    </script>
</body>

</html>
```

**输出:**

```
7
undefined
```

**参考:**T2】https://underscorejs.org/#result