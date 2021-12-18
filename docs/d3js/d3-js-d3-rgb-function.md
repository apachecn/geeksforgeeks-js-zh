# D3.js | d3.rgb()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-rgb-function/](https://www.geeksforgeeks.org/d3-js-d3-rgb-function/)

D3.js 中的 **d3.rgb()函数**用于返回指定 CSS 颜色的 rgb 值。

**语法:**

```
d3.rgb(color);
```

**参数:**该功能接受单参数**颜色**，用于指定 CSS 颜色。

**返回值:**该函数返回给定 CSS 颜色的 RGB 值。

以下程序说明了 D3.js 中的 **d3.rgb()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.rgb() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Calling the d3.rgb() function function
        // with some parameters
        var color1 = d3.rgb("red");
        var color2 = d3.rgb("green");
        var color3 = d3.rgb("blue");

        // Getting the RGB values
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
    <title>d3.rgb() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Calling the d3.rgb() function function
        // without any parameters
        var color = d3.rgb();

        // Getting the RGB values
        console.log(color);
    </script>
</body>

</html>
```

**输出:**

```
{"r":null, "g":null, "b":null, "opacity":1}

```

**参考:**T2】https://devdocs.io/d3~5/d3-color#rgb