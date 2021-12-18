# Fabric.js toRgba()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-torgba-method/](https://www.geeksforgeeks.org/fabric-js-torgba-method/)

**toRgba()方法**用于将任何类型的指定颜色表示转换为其 Rgba(红绿蓝和阿尔法)表示。

**语法:**

```
toRgba()
```

**参数:**此方法不接受任何参数。

**返回值:**此方法返回 RGBA 格式的颜色表示。

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

 // Calling the toRgba() function over 
 // the specified color values
 console.log(new fabric.Color("hsl(0, 100%, 50%)").toRgba());
 console.log(new fabric.Color("hsla(10, 40%, 53%, 0.6)").toRgba());
</script>

</body>

</html>
```

**输出:**

```
rgba(255,0,0,1)
rgba(183,103,87,0.6)
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
 var A = "hex(fff00f)";
 var B = "hsl(12, 13%, 25%)";

 // Calling the toRgba() function over 
 // the above specified color values
 console.log(new fabric.Color(A).toRgba());
 console.log(new fabric.Color(B).toRgba());
</script>

</body>

</html>
```

**输出:**

```
rgba(0,0,0,1)
rgba(72,59,55,1)
```