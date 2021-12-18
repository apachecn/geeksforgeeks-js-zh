# fabric . js to exa()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-tohexa-method/](https://www.geeksforgeeks.org/fabric-js-tohexa-method/)

方法用于将任何类型的指定颜色表示转换为其 Hexa(十六进制 alpha)表示。

**语法:**

```
toHexa()
```

**参数:**此方法不接受任何参数。

**返回值:**该方法以 HEXA 格式返回颜色表示。

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

 // Calling the toHexa() function over 
 // the specified color values
 console.log(new fabric.Color("rgb(10, 120, 150)").toHexa());
 console.log(new fabric.Color("hsl(5%, 10%, 250%)").toHexa());
</script>

</body>

</html>
```

**输出:**

```
0A7896FF
000000FF
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
 var C = "hsl(0, 100%, 50%)";
 var D = "hsla(10%, 0, 0, 0.2)";

 // Calling the toHexa() function over 
 // the above specified color values
 console.log(new fabric.Color(A).toHexa());
 console.log(new fabric.Color(B).toHexa());
 console.log(new fabric.Color(C).toHexa());
 console.log(new fabric.Color(D).toHexa());
</script>

</body>

</html>
```

**输出:**

```
000C32FF
0A0DFA1A
FF0000FF
000000FF
```