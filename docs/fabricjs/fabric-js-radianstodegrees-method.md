# Fabric.js radiansToDegrees()方法

> 原文:[https://www . geesforgeks . org/fabric-js-radianstode grees-method/](https://www.geeksforgeeks.org/fabric-js-radianstodegrees-method/)

**radiansToDegrees()方法**用于将指定的弧度值转换为其对应的度数值。

**语法:**

```
radiansToDegrees( radians )
```

**参数:**该方法接受如上所述的参数，如下所述:

*   **弧度:**此参数保存指定的弧度值。

**返回值:**该方法返回转换后的度数值。

**例 1:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <!-- Adding the FabricJS library -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <script type="text/javascript">

        // Calling radiansToDegrees() function over
        // some specified radian values
        console.log(fabric.util.radiansToDegrees(1));
        console.log(fabric.util.radiansToDegrees(5));
        console.log(fabric.util.radiansToDegrees(8));
    </script>
</body>

</html>
```

**输出:**

```
57.29577951308232
286.4788975654116
458.3662361046586
```

**例 2:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <!-- Adding the FabricJS library -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <script type="text/javascript">

        // Specifying some radian values
        var a = 1.2;
        var b = 0.45;

        // Calling radiansToDegrees() function over
        // the above specified radian values
        console.log(fabric.util.radiansToDegrees(a));
        console.log(fabric.util.radiansToDegrees(b));
    </script>
</body>

</html>
```

**输出:**

```
68.75493541569878
25.783100780887047
```