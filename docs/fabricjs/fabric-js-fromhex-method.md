# Fabric.js fromHex()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-fromhex-method/](https://www.geeksforgeeks.org/fabric-js-fromhex-method/)

**fromHex()方法**用于以 Hex 格式返回指定颜色的新颜色对象。

**语法:**

```
fromHex(color)
```

**参数:**该方法接受如上所述的参数，如下所述:

*   **颜色:**此参数保存 HEX 格式的指定字符串颜色值。

**返回值:**该方法以 HEX 格式为指定颜色返回“RGBA(红-绿-蓝-阿尔法)”格式的新颜色对象。

**例 1:**

## java 描述语言

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

   // Calling the fromHex() function over
   // the specified color value in HEX format
   console.log(fabric.Color.fromHex("FF0000")); 
  </script>
</body>

</html>
```

**输出:**

```
{"_source":[255,0,0,1]}
```

**例 2:**

## java 描述语言

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

   // Initializing some color values in HEX format
   var Green = "00FF00";
   var Blue = "0000FF";
   var Yellow = "FFFF00";

   // Calling the fromHex() function over
   // the above specified color values
   console.log(fabric.Color.fromHex(Green)); 
   console.log(fabric.Color.fromHex(Blue)); 
   console.log(fabric.Color.fromHex(Yellow)); 
  </script>
</body>

</html>
```

**输出:**

```
{"_source":[0,255,0,1]}
{"_source":[0,0,255,1]}
{"_source":[255,255,0,1]}
```