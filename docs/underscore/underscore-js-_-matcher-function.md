# 下划线. js _。匹配器()功能

> 原文:[https://www . geesforgeks . org/下划线-js-_-matcher-function/](https://www.geeksforgeeks.org/underscore-js-_-matcher-function/)

**下划线. js** 是一个 JavaScript 库，它提供了很多有用的函数，在很大程度上有助于编程，比如映射、过滤、调用等。即使不使用任何内置对象。

**_。matcher()函数**是 JavaScript 的下划线. js 库中的一个内置函数，用于查找谓词函数，该函数可以通知您传入的对象是否包含所有在 *attrs* 参数中给出的键值属性。

**语法:**

```
_.matcher(attrs)
```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **属性:**是具有键和值对的属性。

**返回值:**这个方法返回一个谓词函数。

**例 1:**

## Javascript

```
<!DOCTYPE html>
<html>

<head>
    <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.11.0/underscore.js"></script>
</head>

<body>
    <script type="text/javascript">
        console.log(_.matcher({ 
            picked: true, seeable: false 
        }));
    </script>
</body>

</html>
```

**输出:**

```
function(obj) { return isMatch(obj, attrs); }
```

**例二:**

## Javascript

```
<!DOCTYPE html>
<html>

<head>
    <script type="text/javascript"
        src=
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.11.0/underscore.js"></script>
</head>

<body>
    <script type="text/javascript">
        var attr = "GeeksforGeeks";
        console.log(_.matcher(attr));
    </script>
</body>

</html>
```

**输出:**

```
function(obj) { return isMatch(obj, attrs); }
```

**参考:**T2】https://underscorejs.org/#matcher