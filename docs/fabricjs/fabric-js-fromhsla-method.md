# Fabric.js fromHsla()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-fromhsla-method/](https://www.geeksforgeeks.org/fabric-js-fromhsla-method/)

方法用于为 Hsla(色调、饱和度、亮度和 alpha)格式的指定颜色返回一个新的颜色对象。

**语法:**

```
fromHsla(color)
```

**参数:**该方法接受如上所述的参数，如下所述:

*   **颜色:**此参数保存 HSLA 格式的指定字符串颜色值。

**返回值:**该方法为 HSLA 格式的指定颜色返回“RGBA(红-绿-蓝-阿尔法)”格式的新颜色对象。

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

   // Calling the fromHsla() function over
   // the specified color value in HSLA format
   console.log(fabric.Color
      .fromHsla("hsla(0, 100%, 50%, 1.0)")); 
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

   // Initializing some color values in HSLA format
   var Black = "hsla(0, 0% ,0%, 0.1)";
   var Red = "hsla(0, 100%, 50%, 1.0)";

   // Calling the fromHsla() function over
   // the above specified color values
   console.log(fabric.Color.fromHsla(Black)); 
   console.log(fabric.Color.fromHsla(Red)); 
  </script>
</body>

</html>
```

**输出:**

```
{"_source":[0,0,0,0.1]}
{"_source":[255,0,0,1]}
```