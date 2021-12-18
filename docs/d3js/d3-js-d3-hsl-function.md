# D3.js | d3.hsl()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-hsl-function/](https://www.geeksforgeeks.org/d3-js-d3-hsl-function/)

D3.js 中的 **d3.hsl()函数**用于构造新的 hsl 颜色，并返回指定颜色的 HSL 属性作为函数的参数。
**语法:**

```
d3.hsl(h, s, l, opacity)
```

或者

```
d3.hsl(color)
```

**参数:**该功能接受上面提到的和下面描述的一些参数:

*   **h:** 用于设置色相值。
*   **s:** 用于设置饱和度值。
*   **l:** 用于设置明度值。
*   **不透明度:**用于设置不透明度/透明度。
*   **颜色:**用于设置颜色名称或十六进制代码。

**返回值:**该函数返回指定 CSS 颜色的 HSL 属性作为函数的参数。
以下程序说明了 D3.js:
**示例 1:**
中的 **d3.hsl()** 功能

## java 描述语言

```
<!DOCTYPE html>
<html>

 <head>
    <title>
        D3.js | d3.hsl() Function
    </title>

    <script src=
        'https://d3js.org/d3.v4.min.js'>
    </script>
</head>

<body>
    <script>

        // Calling the d3.hsl() function
        // with some parameters
        var color1 = d3.hsl("red");
        var color2 = d3.hsl("green");
        var color3 = d3.hsl("blue");

        // Getting the HSL properties
        console.log(color1);
        console.log(color2);
        console.log(color3);
    </script>
</body>

</html>
```

**输出:**

```
{"h":0, "s":1, "l":0.5, "opacity":1}
{"h":120, "s":1, "l":0.25098039215686274, "opacity":1}
{"h":240, "s":1, "l":0.5, "opacity":1}
```

**例 2:**

## java 描述语言

```
<!DOCTYPE html>
<html>

 <head>
    <title>
        D3.js | d3.hsl() Function
    </title>

    <script src=
        'https://d3js.org/d3.v4.min.js'>
    </script>
</head>

<body>
    <script>

        // Calling the d3.hsl() function
        // without any parameters
        var color = d3.hsl();

        // Getting the HSL values
        console.log(color);
    </script>
</body>

</html>
```

**输出:**

```
{"h":null, "s":null, "l":null, "opacity":1}
```

**参考:t1】[https://devdocs . io/D3 ~ 5/D3-color # HSL](https://devdocs.io/d3~5/d3-color#hsl)**