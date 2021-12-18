# Fabric.js sourceFromHsl()方法

> 原文:[https://www . geesforgeks . org/fabric-js-source from HSL-method/](https://www.geeksforgeeks.org/fabric-js-sourcefromhsl-method/)

方法用于返回 Hsl(色调-饱和度-亮度)或 HSLA(色调-饱和度-亮度-α)格式的指定颜色值的颜色数组表示。

**语法:**

```
sourceFromHsl(color)
```

**参数:**该方法接受如上所述的参数，如下所述:

*   **颜色:**此参数保存 HSL 或 HSLA 格式的指定颜色值。

**返回值:**该方法返回 HSL 或 HSLA 格式的指定颜色值的 RGBA(红绿蓝和阿尔法)格式的值的数组表示。

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

 // Calling the sourceFromHsl() function over
 // the color value in HSL and HSLA format
 console.log(fabric.Color.sourceFromHsl("hsl(0, 100%, 50%)"));
 console.log(fabric.Color.sourceFromHsl("hsla(0, 100%, 50%, 0.6)"));
</script>

</body>

</html>
```

**输出:**

```
[255,0,0,1]
[255,0,0,0.6]
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

 // Initializing some color values in HSL format
 var A = "hsl(0, 100%, 50%)";
 var B = "hsl(0, 0%, 50%)";

 // Initializing some color values in HSLA format
 var C = "hsla(0, 100%, 50%, 0.9)";
 var D = "hsla(0, 0%, 50%, 0.2)";

 // Calling the sourceFromHsl() function over
 // the above color values
 console.log(fabric.Color.sourceFromHsl(A));
 console.log(fabric.Color.sourceFromHsl(B));
 console.log(fabric.Color.sourceFromHsl(C));
 console.log(fabric.Color.sourceFromHsl(D));
</script>

</body>

</html>
```

**输出:**

```
[255,0,0,1]
[128,128,128,1]
[255,0,0,0.9]
[128,128,128,0.2]
```