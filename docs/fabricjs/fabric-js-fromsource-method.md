# Fabric.js fromSource()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-fromsource-method/](https://www.geeksforgeeks.org/fabric-js-fromsource-method/)

**fromSource()方法**用于为数组表示中的指定颜色返回一个新的颜色对象，其值采用 RGBA(红绿蓝和阿尔法)格式。

**语法:**

```
fromSource( source )
```

**参数:**该方法接受如上所述的参数，如下所述:

*   **来源:**此参数保存 RGBA 格式的指定值数组。

**返回值:**该方法为数组中的指定颜色返回一个“RGBA(红-绿-蓝-阿尔法)”格式的新颜色对象。

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

        // Calling the fromSource() function
        // over the array of specified color
        // value in RGBA format
        console.log(fabric.Color
            .fromSource([200, 100, 100, 0.5]));
    </script>
</body>

</html>
```

**输出:**

```
{"_source":[200,100,100,0.5]}
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

        // Initializing some arrays of 
        // color values in RGBA format
        var Black = [0, 0, 0, 1.0];
        var Blue = [0, 0, 255, 0.5];
        var Yellow = [255, 255, 0.9];

        // Calling the fromSource() function over
        // the above array of specified color values
        console.log(fabric.Color.fromSource(Black));
        console.log(fabric.Color.fromSource(Blue));
        console.log(fabric.Color.fromSource(Yellow));
    </script>
</body>

</html>
```

**输出:**

```
{"_source":[0,0,0,1]}
{"_source":[0,0,255,0.5]}
{"_source":[255,255,0.9]}
```