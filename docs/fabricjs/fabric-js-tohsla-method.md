# fabric . js to SLA()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-tohsla-method/](https://www.geeksforgeeks.org/fabric-js-tohsla-method/)

方法用于将任何类型的指定颜色表示转换为 Hsla(色调、饱和度、亮度和 alpha)表示。

**语法:**

```
toHsla()
```

**参数:**此方法不接受任何参数。

**返回值:**此方法返回 HSLA 格式的颜色表示。

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

 // Calling the toHsla() function over 
 // the specified color values
 console.log(new fabric.Color("rgb(10, 120, 150)").toHsla());
 console.log(new fabric.Color("rgba(100, 20, 255, 0.3)").toHsla());
</script>

</body>

</html>
```

**输出:**

```
hsla(193,88%,31%,1)
hsla(260,100%,54%,0.3)
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
 var C = "hex(ffffff)";

 // Calling the toHsla() function over 
 // the above specified color values
 console.log(new fabric.Color(A).toHsla());
 console.log(new fabric.Color(B).toHsla());
 console.log(new fabric.Color(C).toHsla());
</script>

</body>

</html>
```

**输出:**

```
hsla(226,100%,10%,1)
hsla(239,96%,51%,0.1)
hsla(0,0%,0%,1)
```