# Fabric.js sourceFromHex()方法

> 原文:[https://www . geesforgeks . org/fabric-js-source from hex-method/](https://www.geeksforgeeks.org/fabric-js-sourcefromhex-method/)

**sourceFromHex()方法**用于以十六进制(十六进制)格式返回指定颜色值的颜色数组表示。

**语法:**

```
sourceFromHex( color )
```

**参数:**该方法接受如上所述的参数，如下所述:

*   **颜色:**该参数保存 HEX 格式的指定颜色值。

**返回值:**这个方法返回一个 RGBA(红绿蓝和阿尔法)格式的值的数组表示，该值是十六进制格式的指定颜色值的颜色。

**例 1:**

## java 描述语言

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

        // Calling the sourceFromHex() function over
        // the color value in HEX format
        console.log(fabric.Color.sourceFromHex("FF00FF"));
    </script>
</body>

</html>
```

**输出:**

```
[255, 0, 255, 1]
```

**例 2:**

## java 描述语言

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

        // Initializing some color values in HEX format
        var Purple = "800080";
        var Lime = "00FF00";
        var Yellow = "FFFF00";

        // Calling the sourceFromHex() function over
        // the above color values
        console.log(fabric.Color.sourceFromHex(Purple));
        console.log(fabric.Color.sourceFromHex(Lime));
        console.log(fabric.Color.sourceFromHex(Yellow));
    </script>
</body>

</html>
```

**输出:**

```
[128,0,128,1]
[0,255,0,1]
[255,255,0,1]
```