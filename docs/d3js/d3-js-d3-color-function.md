# D3.js | d3.color()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-color-function/](https://www.geeksforgeeks.org/d3-js-d3-color-function/)

D3.js 中的 **d3.color()函数**用于解析作为函数参数的指定 CSS 颜色，并返回 [RGB](https://www.geeksforgeeks.org/computer-graphics-the-rgb-color-model/) 或 [HSL](https://www.geeksforgeeks.org/html-color-styles-hsl/) 颜色。如果未给出说明符，则返回 null。

**语法:**

```
d3.color(color);
```

**参数:**该功能接受单参数**颜色**，指定 CSS 颜色。

**返回值:**该函数返回作为函数参数的指定 CSS 颜色的 RGB 或 HSL 颜色值。

以下程序说明了 D3.js 中的 **d3.color()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.color() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Calling the d3.color() function function
        // with some parameters
        var color1 = d3.color("red");
        var color2 = d3.color("green");
        var color3 = d3.color("blue");

        // Getting the RGB or HSL values
        console.log(color1);
        console.log(color2);
        console.log(color3);
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
    <title>d3.color() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Calling the d3.color() function function
        // without any parameters
        var color = d3.color();

        // Getting the RGB or HSL values
        console.log(color);
    </script>
</body>

</html>
```

**输出:**

```
null

```

**参考:**T2】https://devdocs.io/d3~5/d3-color#color