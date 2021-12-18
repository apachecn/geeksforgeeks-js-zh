# D3.js | color.opacity

> 原文:[https://www.geeksforgeeks.org/d3-js-color-opacity/](https://www.geeksforgeeks.org/d3-js-color-opacity/)

D3.js 中的**颜色不透明度**用于淡化颜色。不透明度值在[0，1]的范围内。

**语法:**

```
color.opacity
```

**参数:**此功能不接受任何参数。

**返回值:**该函数返回指定颜色的不透明度值。

下面的程序说明了 D3.js 中的 **color.opacity** 功能:

**例:**

```
<!DOCTYPE html>
<html>

<head>
    <title>color.rgb() function</title>

    <script src='https://d3js.org/d3.v4.min.js'>
  </script>
</head>

<body>
    <script>
        // Calling the d3.color() function
        // with some parameters
        var color1 = d3.color("red");
        var color2 = d3.color("green");
        var color3 = d3.color("blue");

        // Calling the color.opacity
        var A = color1.opacity;
        var B = color2.opacity;
        var C = color3.opacity;

        // Getting the opacity value
        console.log(A);
        console.log(B);
        console.log(C);
    </script>
</body>

</html>
```

**输出:**

```
1
1
1

```

**参考:t1】[https://devdocs . io/D3 ~ 5/D3-color # color _ opacity](https://devdocs.io/d3~5/d3-color#color_opacity)**