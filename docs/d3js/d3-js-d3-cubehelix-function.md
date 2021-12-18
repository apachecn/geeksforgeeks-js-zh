# D3.js | d3.cubehelix()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-cubehelix-function/](https://www.geeksforgeeks.org/d3-js-d3-cubehelix-function/)

D3.js 中的 **d3.cubehelix()函数**用于构造新的 cubehelix 颜色，并返回指定颜色的 HSL 属性作为函数的参数。

**语法:**

```
d3.cubehelix(color);
```

**参数:**该功能接受单参数**颜色**，指定 CSS 颜色。

**返回值:**该函数返回指定 CSS 颜色的 HSL 属性作为函数的参数。

下面的程序说明了 D3.js 中的 **d3.cubehelix()** 函数:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.cubehelix() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Calling the d3.cubehelix() function function
        // with some parameters
        var color1 = d3.cubehelix("red");
        var color2 = d3.cubehelix("green");
        var color3 = d3.cubehelix("blue");

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
{"h":351.8102617708421, "s":1.9488976453722686, "l":0.2999994453152424, "opacity":1}
{"h":109.95916521883123, "s":1.1193720244160954, "l":0.29615736727228126, "opacity":1}
{"h":236.94217167732103, "s":4.614386868039719, "l":0.10999954957200976, "opacity":1}

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.cubehelix() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Calling the d3.cubehelix() function function
        // without any parameters
        var color = d3.cubehelix();

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

**参考:**T2】https://devdocs.io/d3~5/d3-color#cubehelix