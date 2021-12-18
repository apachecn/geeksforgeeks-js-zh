# Fabric.js getSource()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-getsource-method/](https://www.geeksforgeeks.org/fabric-js-getsource-method/)

**getSource()方法**用于获取指定颜色值的来源。

**语法:**

```
getSource()
```

**参数:**此方法不接受任何参数。

**返回值:**此方法返回指定颜色值的来源。返回的源值将以数组形式表示。

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

 // Calling the getSource() function over
 // the specified color values
 console.log(new fabric.Color("hsl(0, 100%, 50%)").getSource());
 console.log(new fabric.Color("hsla(10%, 100%, 50%, 0.2)").getSource());
</script>

</body>

</html>
```

**输出:**

```
[255,0,0,1]
[0,0,0,1]
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
 var C = "hsla(10, 40%, 13%, 0.6)";
 var D = "rgb(10, 40, 13)";
 var E = "rgba(10, 40, 13, 0.9)";

 // Calling the getSource() function over
 // the above specified color values
 console.log(new fabric.Color(A).getSource());
 console.log(new fabric.Color(B).getSource());
 console.log(new fabric.Color(C).getSource());
 console.log(new fabric.Color(D).getSource());
 console.log(new fabric.Color(E).getSource());
</script>

</body>

</html>
```

**输出:**

```
[0,0,0,1]
[72,59,55,1]
[46,24,20,0.6]
[10,40,13,1]
[10,40,13,0.9]
```