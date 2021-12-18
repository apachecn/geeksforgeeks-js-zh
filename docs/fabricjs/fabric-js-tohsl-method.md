# Fabric.js toHsl()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-tohsl-method/](https://www.geeksforgeeks.org/fabric-js-tohsl-method/)

方法用于将任何类型的指定颜色表示转换为其 Hsl(色调、饱和度和亮度)表示。

**语法:**

```
toHsl()
```

**参数:**此方法不接受任何参数。

**返回值:**此方法返回 HSL 格式的颜色表示。

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

 // Calling the toHsl() function over 
 // the specified color values
 console.log(new fabric.Color("rgb(10, 120, 150)").toHsl());
 console.log(new fabric.Color("hex(0A7000FF)").toHsl());
</script>

</body>

</html>
```

**输出:**

```
hsl(193,88%,31%)
hsl(0,0%,0%)
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

 // Initializing some color values in different color format
 var A = "rgb(0, 12, 50)";
 var B = "rgba(10, 13, 250, 0.1)";
 var C = "hex(ff0000)";

 // Calling the toHsl() function over 
 // the above specified color values
 console.log(new fabric.Color(A).toHsl());
 console.log(new fabric.Color(B).toHsl());
 console.log(new fabric.Color(C).toHsl());
</script>

</body>

</html>
```

**输出:**

```
hsl(226,100%,10%)
hsl(239,96%,51%)
hsl(0,0%,0%)
```