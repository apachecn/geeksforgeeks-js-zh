# Fabric.js overlayWith()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-overlaywith-method/](https://www.geeksforgeeks.org/fabric-js-overlaywith-method/)

**overlayWith()方法**用于以给定颜色为参数覆盖给定颜色。

**语法:**

```
overlayWith(otherColor)
```

**参数:**该方法接受如上所述的参数，如下所述:

*   **其他颜色:**该参数保存指定的颜色。

**返回值:**此方法返回叠加的颜色。

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

 // Calling the overlayWith() function over
 // the specified color values
 console.log(new fabric.Color("rgb(10, 40, 13)").overlayWith("rgb(10, 41, 13, 1)"));
</script>

</body>

</html>
```

**输出:**

```
{"_source":[10,41,13,1]}
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
 var B = "hsl(12%, 13%, 25%)";
 var C = "hsla(10%, 40%, 13%, 0.6)";

 // Calling the overlayWith() function over
 // the above specified color values
 console.log(new fabric.Color(A).overlayWith("rgb(10, 41, 13, 1)"));
 console.log(new fabric.Color(A).overlayWith("rgba(1, 4, 3, 0.2)"));
 console.log(new fabric.Color(A).overlayWith("hex(ffffff)"));
</script>

</body>

</html>
```

**输出:**

```
{"_source":[5,21,7,1]}
{"_source":[1,2,2,1]}
{"_source":[0,0,0,1]}
```