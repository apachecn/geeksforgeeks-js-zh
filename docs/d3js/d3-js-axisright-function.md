# D3.js axisRight()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-axisright-function/](https://www.geeksforgeeks.org/d3-js-axisright-function/)

轴可以使用内置的 D3 函数绘制。它由线条、记号和标签组成。D3.js 中的 **d3.axisRight()函数**用于创建一个垂直的右向轴。该函数将为给定的刻度构造一个新的右向轴生成器，带有空刻度参数，刻度大小为 6，填充为 3。

Axis API 可以使用以下脚本进行配置。

```
<script src = "https://d3js.org/d3-axis.v1.min.js"></script>

```

**语法:**

```
d3.axisRight( scale )
```

**参数:**该函数只接受一个参数，如上所述，如下所述:

*   **刻度:**该参数保存使用的刻度。

**返回值:**该函数返回创建的垂直向右轴。

以下程序说明了 D3.js 中的 **d3.axisRight()** 功能:

**例 1:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.axisRight() Function
    </title>
    <script type="text/javascript" 
        src="https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>
        var width = 400, height = 400;
        var svg = d3.select("body")
            .append("svg")
            .attr("width", width)
            .attr("height", height);

        var yscale = d3.scaleLinear()
            .domain([0, 100])
            .range([height - 50, 0]);

        var y_axis = d3.axisRight(yscale);

        svg.append("g")
            .attr("transform", "translate(100,10)")
            .call(y_axis)
    </script>
</body>

</html>
```

**输出:**

![](img/aa22ac45203e6e2dad26579cdfbc6a01.png)

**例 2:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.axisRight() Function
    </title>
    <script type="text/javascript" 
        src="https://d3js.org/d3.v4.min.js">
    </script>

    <style>
        svg text {
            fill: green;
            font: 15px sans-serif;
            text-anchor: start;
        }
    </style>
</head>

<body>
    <script>
        var width = 400, height = 400;
        var data = [10, 12, 14, 16, 18, 20];
        var svg = d3.select("body")
            .append("svg")
            .attr("width", width)
            .attr("height", height);

        var yscale = d3.scaleLinear()
            .domain([d3.min(data), d3.max(data)])
            .range([height - 50, 0]);

        var y_axis = d3.axisRight(yscale);

        svg.append("g")
            .attr("transform", "translate(100,20)")
            .call(y_axis)
    </script>
</body>

</html>
```

**输出:**

![](img/ed9773eba10b5cf6119ef3c7f67997f1.png)