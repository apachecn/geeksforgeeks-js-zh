# D3 . js | color . displayed()函数

> 原文:[https://www . geesforgeks . org/D3-js-color-displayed-function/](https://www.geeksforgeeks.org/d3-js-color-displayable-function/)

D3.js 中的**color . displayed()函数**用于在颜色可显示的情况下返回 true，否则返回 false。

**语法:**

```
color.displayable()
```

**参数:**此功能不接受任何参数。

**返回值:**如果颜色可显示，则该函数返回真，否则返回假。

下面的程序说明了 D3.js 中的 **color.displayable()** 功能:

**例:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
      color.displayable() function
  </title>

    <script src=
'https://d3js.org/d3.v4.min.js'>
  </script>
</head>

<body>
    <script>
        // Calling the d3.color() function
        // with some parameters
        var color1 = d3.color("red");
        var color2 = d3.color("green");
        var color3 = d3.color("blue");

        // Calling the color.displayable() function
        var A = color1.displayable();
        var B = color2.displayable();
        var C = color3.displayable();

        // Getting the value true or false
        console.log(A);
        console.log(B);
        console.log(C);
    </script>
</body>

</html>
```

**输出:**

```
true
true
true

```

**参考:**T2】https://devdocs.io/d3~5/d3-color#color_displayable