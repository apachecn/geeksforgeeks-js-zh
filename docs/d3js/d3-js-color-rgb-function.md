# D3.js | color.rgb()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-color-rgb-function/](https://www.geeksforgeeks.org/d3-js-color-rgb-function/)

D3.js 中的 **color.rgb()函数**用于返回指定颜色的 rgb 等价物。

**语法:**

```
color.rgb()
```

**参数:**此功能不接受任何参数。

**返回值:**该函数返回指定颜色的 RGB 等效值。

以下程序说明了 D3.js 中的 **color.rgb()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>color.rgb() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Calling the d3.color() function function
        // with some parameters
        var color1 = d3.color("red");
        var color2 = d3.color("green");
        var color3 = d3.color("blue");

        // Calling the color.rgb() function
        var A = color1.rgb();
        var B = color2.rgb();
        var C = color3.rgb();

        // Getting the RGB equivalent of the specified color
        console.log(A);
        console.log(B);
        console.log(C);
    </script>
</body>

</html>
```

**输出:**

```
{"r":255, "g":0, "b":0, "opacity":1}
{"r":0, "g":128, "b":0, "opacity":1}
{"r":0, "g":0, "b":255, "opacity":1}

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>color.rgb() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Calling the d3.rgb() function
        // without any parameters
        var color1 = d3.rgb();

        // Calling the color.rgb() function
        var A = color1.rgb();

        // Getting the RGB equivalent of the specified color
        console.log(A);
    </script>
</body>

</html>
```

**输出:**

```
{"r":null, "g":null, "b":null, "opacity":1}

```

**参考:**T2】https://devdocs.io/d3~5/d3-color#color_rgb