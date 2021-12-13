# D3.js symbolStar 符号

> 原文:[https://www.geeksforgeeks.org/d3-js-symbolstar-symbol/](https://www.geeksforgeeks.org/d3-js-symbolstar-symbol/)

**d3.symbolStar** 是 D3.js 中的符号类型，是可以使用的星形符号类型。

**语法:**

```html
d3.symbolStar
```

**例 1:**

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">

    <script src=
        "https://d3js.org/d3.v5.min.js">
    </script>
</head>

<body>

    <h1 style="text-align: center; 
        color: green;">
        GeeksforGeeks
    </h1>

    <h3 style="text-align: center;">
        D3.js | symbolStar 
    </h3>

    <center>
    <svg id="gfg" width="100"
         height="100"></svg>
    </center>

    <script>
        // symbolStar
        var sym = 
d3.symbol().type(d3.symbolStar).size(500);
        d3.select("#gfg")
            .append("path")
            .attr("d", sym)
            .attr("fill", "green")
            .attr("transform", "translate(50, 50)");

    </script>
</body>

</html>
```

**输出:**

![](img/895649034d18297c42eccc9083829260.png)

**例 2:**

```html
<!DOCTYPE html>
    <html>
    <head>
        <meta charset="utf-8">

        <script src=
            "https://d3js.org/d3.v5.min.js">
        </script>
    </head>

    <body>

        <h1 style="text-align: center;
            color: green;">
            GeeksforGeeks
        </h1>

        <h3 style="text-align: center;">
            D3.js | symbolStar
        </h3>

        <center>
        <svg id="gfg" width="100"
             height="100"></svg>
        </center>

        <script>
            // symbolStar 
            var sym = 
d3.symbol().type(d3.symbolStar).size(500);
            d3.select("#gfg")
                .append("path")
                .attr("d", sym)
                .attr("fill", "none")
                .attr("stroke", "green")
                .attr("stroke-width", "5px")
                .attr("transform", "translate(50, 50)");
        </script>
    </body>

    </html>
```

**输出:**

![](img/8cdb7b8602cf062642099b5edc5f98a9.png)