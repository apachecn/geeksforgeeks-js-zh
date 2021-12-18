# fabric . js . toGrayscale()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-tograyscale-method/](https://www.geeksforgeeks.org/fabric-js-tograyscale-method/)

**灰度()方法**用于将任何类型的指定颜色表示转换为其灰度表示。

**语法:**

```
toGrayscale()
```

**参数:**此方法不接受任何参数。

**返回值:**此方法返回灰度表示中的颜色表示。

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
        // Calling the toGrayscale() function over 
        // the specified color values
        console.log(new fabric.Color("hsl(0, 100%, 50%)")
                                      .toGrayscale());
        console.log(new fabric.Color("hsla(10, 40%, 53%, 0.6)")
                                      .toGrayscale());
        </script>
    </body>

</html>
```

**输出:**

```
{"_source":[77,77,77,1]}
{"_source":[125,125,125,0.6]}
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

    // Calling the toGrayscale() function over 
    // the above specified color values
    console.log(new fabric.Color(A).toGrayscale());
    console.log(new fabric.Color(B).toGrayscale());
    console.log(new fabric.Color(C).toGrayscale());
    console.log(new fabric.Color(D).toGrayscale());
    </script>

</body>

</html>
```

**输出:**

```
{"_source":[0,0,0,1]}
{"_source":[62,62,62,1]}
{"_source":[30,30,30,0.6]}
{"_source":[28,28,28,1]}
```