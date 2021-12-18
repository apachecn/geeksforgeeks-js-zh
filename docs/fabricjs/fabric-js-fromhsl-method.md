# Fabric.js fromHsl()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-fromhsl-method/](https://www.geeksforgeeks.org/fabric-js-fromhsl-method/)

**fromHsl()方法**用于为 Hsl(色相-饱和度-明度)格式的指定颜色返回一个新的颜色对象。

**语法:**

```
fromHsl(color)
```

**参数:**该方法接受如上所述的参数，如下所述:

*   **颜色:**此参数保存 HSL 格式的指定字符串颜色值。

**返回值:**该方法为 HSL 格式的指定颜色返回“RGBA(红-绿-蓝-阿尔法)”格式的新颜色对象。

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

   // Calling the fromHsl() function over
   // the specified color value in HSL format
   console.log(fabric.Color.fromHsl("hsl(0, 100%, 50%)")); 
  </script>
</body>

</html>
```

**输出:**

```
{"_source":[255,0,0,1]}
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

   // Initializing some color values in HSL format
   var Green = "hsl(120, 100%, 50%)";
   var Blue = "hsl(240, 100%, 50%)";

   // Calling the fromHsl() function over
   // the above specified color values
   console.log(fabric.Color.fromHsl(Green)); 
   console.log(fabric.Color.fromHsl(Blue)); 
  </script>
</body>

</html>
```

**输出:**

```
{"_source":[0,255,0,1]}
{"_source":[0,0,255,1]}
```