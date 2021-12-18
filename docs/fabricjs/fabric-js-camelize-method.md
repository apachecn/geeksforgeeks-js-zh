# 布艺山茶花()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-camelize-method/](https://www.geeksforgeeks.org/fabric-js-camelize-method/)

**茶化()方法**用于茶化指定的字符串。

**语法:**

```
camelize(string)
```

**参数:**该方法接受一个如上所述的参数，如下所述:

*   **String:** This parameter saves the string for camellias.

**返回值:**这个方法返回字符串的驼化版本。

**例 1:**

## Javascript

```
<!DOCTYPE html>
<html>

<head>
    <!-- Loading the FabricJS library -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <script type="text/javascript">
        console.log(fabric.util.string.camelize("a-ab-abc"));
    </script>
</body>

</html>
```

**输出:**

```
aAbAbc
```

**例二:**

## Javascript

```
<!DOCTYPE html>
<html>

<head>
    <!-- Loading the FabricJS library -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <script type="text/javascript">
        console.log(fabric.util.string.camelize("geeks-for-geeks"));
    </script>
</body>

</html>
```

**输出:**

```
geeksForGeeks
```

**参考:**T2】http://fabricjs.com/docs/fabric.util.string.html#.camelize