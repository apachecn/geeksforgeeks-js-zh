# D3.js 符号. size()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-symbol-size-method/](https://www.geeksforgeeks.org/d3-js-symbol-size-method/)

可以使用 **符号大小()方法** 来改变符号的大小。

**语法:**

```
symbol.size([size])

```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **大小:**这是平方像素中的大小或者是要设置的区域。

**返回值:**这个方法没有返回值。

**例 1:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">

    <script src=
        "https://d3js.org/d3.v5.min.js">
    </script>
</head>

<body>

    <h1 style="text-align: center; color: green;">
        GeeksforGeeks
    </h1>

    <h3 style="text-align: center;">
        D3.js | symbol.size() Method
    </h3>

    <center>
    <svg id="gfg" width="100" height="100"></svg>
    </center>

    <script>
        var sym = d3.symbol().size(300);
        d3.select("#gfg")
            .append("path")
            .attr("d", sym)
            .attr("fill", "green")
            .attr("transform", "translate(50,50)");

    </script>
</body>

</html>
```

**输出:**

![](img/dabba9fc45f2e2d5123d0664e2b37aef.png)

**例 2:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">

    <script src=
        "https://d3js.org/d3.v5.min.js">
    </script>
</head>

<body>

    <h1 style="text-align: center; color: green;">
        GeeksforGeeks
    </h1>

    <h3 style="text-align: center;">
        D3.js | symbol.size() Method
    </h3>

    <center>
    <svg id="gfg" width="100" height="100"></svg>
    </center>

    <script>
        var sym = d3.symbol().size(500);
        d3.select("#gfg")
            .append("path")
            .attr("d", sym)
            .attr("fill", "none")
            .attr("stroke", "green")
            .attr("stroke-width", "5px")
            .attr("transform", "translate(50,50)");

    </script>
</body>

</html>
```

**输出:**

![](img/0bfc787e643353d7c4b9320df97f5f42.png)