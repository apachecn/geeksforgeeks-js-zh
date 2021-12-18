# D3.js | color.toString()函数

> 原文:[https://www . geesforgeks . org/D3-js-color-tostring-function/](https://www.geeksforgeeks.org/d3-js-color-tostring-function/)

D3.js 中的 **color.toString()函数**用于根据 CSS 对象模型规范返回表示颜色的字符串。

**语法:**

```
color.toString()
```

**参数:**此功能不接受任何参数。

**返回值:**这个函数根据 CSS 对象模型规范返回一个表示颜色的字符串。

下面的程序说明了 D3.js 中的 **color.toString()** 函数:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>color.toString() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Calling the d3.color() function function
        // with some parameters
        var color1 = d3.color("red");
        var color2 = d3.color("green");
        var color3 = d3.color("blue");

        // Calling the color.toString() function
        var A = color1.toString();
        var B = color2.toString();
        var C = color3.toString();

        // Getting the string representing
        console.log(A);
        console.log(B);
        console.log(C);
    </script>
</body>

</html>
```

**输出:**

```
rgb(255, 0, 0)
rgb(0, 128, 0)
rgb(0, 0, 255)

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>color.toString() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Calling the d3.rgb() function
        // without some parameters
        var color = d3.rgb();

        // Calling the color.toString() function
        var A = color.toString();

        // Getting the string representing
        console.log(A);
    </script>
</body>

</html>
```

**输出:**

```
rgb(0, 0, 0)

```

**参考:**T2】https://devdocs.io/d3~5/d3-color#color_toString