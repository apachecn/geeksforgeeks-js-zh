# Fabric.js toRgb()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-torgb-method/](https://www.geeksforgeeks.org/fabric-js-torgb-method/)

**toRgb()方法**用于将任何类型的指定颜色表示转换为其 Rgb(红绿蓝)表示。

**语法:**

```
toRgb()
```

**参数:**此方法不接受任何参数。

**返回值:**此方法返回 RGB 格式的颜色表示。

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

 // Calling the toRgb() function over 
 // the specified color values
 console.log(new fabric.Color("hsl(0, 100%, 50%)").toRgb());
 console.log(new fabric.Color("hsla(10, 40%, 53%, 0.6)").toRgb());
</script>

</body>

</html>
```

**输出:**

```
rgb(255,0,0)
rgb(183,103,87)
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

 // Calling the toRgb() function over 
 // the above specified color values
 console.log(new fabric.Color(A).toRgb());
 console.log(new fabric.Color(B).toRgb());
</script>

</body>

</html>
```

**输出:**

```
rgb(0,0,0)
rgb(72,59,55)
```