# Fabric.js 大写()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-capitalize-method/](https://www.geeksforgeeks.org/fabric-js-capitalize-method/)

用于大写指定字符串的**大写()方法**。

**语法:**

```
capitalize(string, firstLetterOnly)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **字符串:**此参数保存需要大写的字符串。
*   **firstLetterOnly:** 该参数为可选参数，保存布尔值。如果为真，则只有第一个字母大写，其他字母保持不变；如果为假，则第一个字母大写，其他字母转换为小写。

**返回值:**这个方法返回字符串的大写版本。

**例 1:**

## java 描述语言

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
        console.log(fabric.util.string.capitalize("gFG", true));
    </script>
</body>

</html>
```

**输出:**

```
GFG
```

**例 2:**

## java 描述语言

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
        console.log(fabric.util.string.capitalize("gFG", false));
    </script>
</body>

</html>
```

**输出:**

```
Gfg
```