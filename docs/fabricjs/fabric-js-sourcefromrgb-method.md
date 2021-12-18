# Fabric.js sourceFromRgb()方法

> 原文:[https://www . geesforgeks . org/fabric-js-source from RGB-method/](https://www.geeksforgeeks.org/fabric-js-sourcefromrgb-method/)

**sourceFromRgb()方法**用于返回 Rgb(红绿蓝)或 RGBA(红绿蓝阿尔法)格式的指定颜色值的颜色数组表示。

**语法:**

```
sourceFromRgb(color)
```

**参数:**该方法接受如上所述的参数，如下所述:

*   **颜色:**此参数保存 RGB 或 RGBA 格式的指定颜色值。

**返回值:**该方法返回 RGB 或 RGBA 格式的指定颜色值的 RGBA(红绿蓝和阿尔法)格式的值的数组表示。

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

 // Calling the sourceFromRgb() function over
 // the color values in RGB and RGBA format
 console.log(fabric.Color.sourceFromRgb("rgb(13, 50, 77)"));
 console.log(fabric.Color.sourceFromRgb("rgba(200, 255, 252, 0.6)"));
</script>

</body>

</html>
```

**输出:**

```
[13,50,77,1]
[200,255,252,0.6]
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

 // Initializing some color values in RGB format
 var A = "rgb(0, 12, 50)";
 var B = "rgb(254, 200, 110)";

 // Initializing some color values in RGBA format
 var C = "rgba(5, 10, 50, 0.9)";
 var D = "rgba(12, 0, 150, 0.2)";

 // Calling the sourceFromRgb() function over
 // the above color values
 console.log(fabric.Color.sourceFromRgb(A));
 console.log(fabric.Color.sourceFromRgb(B));
 console.log(fabric.Color.sourceFromRgb(C));
 console.log(fabric.Color.sourceFromRgb(D));
</script>

</body>

</html>
```

**输出:**

```
[0,12,50,1]
[254,200,110,1]
[5,10,50,0.9]
[12,0,150,0.2]
```