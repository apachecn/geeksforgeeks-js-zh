# 下划线. js _。求反()函数

> 原文:[https://www . geesforgeks . org/下划线-js-_-求反-函数/](https://www.geeksforgeeks.org/underscore-js-_-negate-function/)

**下划线. js** 是一个 JavaScript 库，它提供了许多有用的函数，这些函数在很大程度上有助于编程，比如映射、过滤、调用等，甚至不使用任何内置对象。

**_。否定()函数**是 JavaScript 的下划线. js 库中的一个内置函数，用于查找所述谓词函数的新的否定版本。

**语法:**

```
_.negate(predicate)
```

**参数:**它接受以下指定的单个参数:

*   **谓语:**是陈述的谓语功能。

**返回值:**该方法返回所述谓词函数的一个新的求反版本。

**例 1:**

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
        var isNaN = _.negate(Boolean);

        console.log(_.find(
            [3, -11, undefined, 41, 0], isNaN));
    </script>
</body>

</html>
```

**输出:**

```
undefined
```

**例 2:**

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
        function isCSportal(character) {
            return character === "GeeksforGeeks";
        }

        var isNotCSportal = _.negate(isCSportal);
        console.log(isNotCSportal("GeeksforGeeks"));
        console.log(isNotCSportal("GfG"));
    </script>
</body>

</html>
```

**输出:**

```
false
 true
```

**参考:**T2】https://underscorejs.org/#negate