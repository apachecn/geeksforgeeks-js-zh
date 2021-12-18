# Fabric.js toHex()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-tohex-method/](https://www.geeksforgeeks.org/fabric-js-tohex-method/)

方法用于将任何类型的指定颜色表示转换为十六进制表示。

**语法:**

```
toHex()
```

**参数:**此方法不接受任何参数。

**返回值:**该方法以 HEX 格式返回颜色表示。

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

 // Calling the toHex() function over 
 // the specified rgb and rgba color format
 console.log(new fabric.Color('rgb(10, 20, 30)').toHex());
 console.log(new fabric.Color('rgba(22, 255, 120, 0.9)').toHex());
</script>

</body>

</html>
```

**输出:**

```
0A141E
16FF78
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

 // Calling the toHex() function over 
 // the above specified color values
 console.log(new fabric.Color(A).toHex());
 console.log(new fabric.Color(B).toHex());
 console.log(new fabric.Color(C).toHex());
 console.log(new fabric.Color(D).toHex());
</script>

</body>

</html>
```

**输出:**

```
000C32
0A0DFA
FF0000
000000
```