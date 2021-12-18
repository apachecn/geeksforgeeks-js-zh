# Fabric.js fromRgb()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-fromrgb-method/](https://www.geeksforgeeks.org/fabric-js-fromrgb-method/)

**fromRgb()方法**用于以 Rgb(红、绿、蓝)格式返回指定颜色的新颜色对象。

**语法:**

```
fromRgb(color)
```

**参数:**该方法接受如上所述的参数，如下所述:

*   **颜色:**此参数保存 RGB 格式的指定字符串颜色值。

**返回值:**该方法为 RGB 格式的指定颜色返回一个“RGBA(红-绿-蓝-阿尔法)”格式的新颜色对象。

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

   // Calling the fromRgb() function over
   // the specified color value in RGB format
   console.log(fabric.Color.fromRgb("rgb(255, 0, 0)")); 
   console.log(fabric.Color.fromRgb("rgb(10, 14, 20)")); 
  </script>

</body>

</html>
```

**输出:**

```
{"_source":[255,0,0,1]}
{"_source":[10,14,20,1]}
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

   // Initializing some color values in RGB format
   var Lime = "rgb(255, 0, 0)";
   var Blue = "rgb(0, 0, 255)";
   var Yellow = "rgb(255, 255, 0)";

   // Calling the fromRgb() function over
   // the above specified color values
   console.log(fabric.Color.fromRgb(Lime)); 
   console.log(fabric.Color.fromRgb(Blue)); 
   console.log(fabric.Color.fromRgb(Yellow)); 
  </script>

</body>

</html>
```

**输出:**

```
{"_source":[255,0,0,1]}
{"_source":[0,0,255,1]}
{"_source":[255,255,0,1]}
```