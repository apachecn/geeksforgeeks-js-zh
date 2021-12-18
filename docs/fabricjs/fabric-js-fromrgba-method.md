# fabric . js frorgba()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-fromrgba-method/](https://www.geeksforgeeks.org/fabric-js-fromrgba-method/)

**frorgba()方法**用于以 Rgba(红绿蓝和阿尔法)格式返回指定颜色的新颜色对象。

**语法:**

```
fromRgba(color)
```

**参数:**该方法接受如上所述的参数，如下所述:

*   **颜色:**此参数保存 RGBA 格式的指定字符串颜色值。

**返回值:**该方法为 RGBA 格式的指定颜色返回“RGBA(红-绿-蓝-阿尔法)”格式的新颜色对象。

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

        // Calling the fromRgba() function over the
        // above specified color value in RGBA format
        console.log(fabric.Color.fromRgba("rgb(0, 0, 128, 0.4)"));
    </script>
</body>

</html>
```

**输出:**

```
{"_source":[0,0,128,0.4]}
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

        // Initializing some color values
        // in RGBA format
        var Black = "rgba(0, 0, 0, 1.0)";
        var Blue = "rgba(0, 0, 255, 0.5)";
        var Yellow = "rgba(255, 255, 0.9)";

        // Calling the fromRgba() function over
        // the above specified color values
        console.log(fabric.Color.fromRgba(Black));
        console.log(fabric.Color.fromRgba(Blue));
        console.log(fabric.Color.fromRgba(Yellow));
    </script>
</body>

</html>
```

**输出:**

```
{"_source":[0,0,0,1]}
{"_source":[0,0,255,0.5]}
{"_source":[255,255,0,1]}
```