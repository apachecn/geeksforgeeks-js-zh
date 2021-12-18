# D3.js axisLeft()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-axisleft-function/](https://www.geeksforgeeks.org/d3-js-axisleft-function/)

轴可以使用内置的 D3 函数绘制。它由线条、记号和标签组成。Axis API 可以使用以下脚本进行配置。

```
<script src = "https://d3js.org/d3-axis.v1.min.js"></script>

```

D3.js 中的 **d3.axisLeft()函数**用于创建左垂直轴。这个函数将为给定的刻度构造一个新的面向左的轴生成器，带有空的刻度参数，刻度大小为 6，填充为 3。

**语法:**

```
d3.axisLeft( scale )

```

**参数:**该函数只接受一个参数，如上所述，如下所述:

*   **刻度:**该参数保存使用的刻度。

**返回值:**该函数返回创建的左垂直轴。

以下程序说明了 D3.js 中的 **d3.axisLeft()** 功能:

**例 1:**

## 超文本标记语言

```
<html>

<head>
    <title>
        D3.js d3.axisLeft() Function
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

        var y_axis = d3.axisLeft(yscale);

        svg.append("g")
            .attr("transform", "translate(100, 10)")
            .call(y_axis)
    </script>
</body>

</html>
```

**输出:**

![](img/639eeb6d782ed8114db2f798d8d2ac63.png)

**例 2:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js d3.axisLeft() Function
    </title>

    <script type="text/javascript" 
        src="https://d3js.org/d3.v4.min.js">
    </script>

    <style>
        svg text {
            fill: green;
            font: 15px sans-serif;
            text-anchor: center;
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

        var y_axis = d3.axisLeft(yscale);

        svg.append("g")
            .attr("transform", "translate(100, 20)")
            .call(y_axis)
    </script>
</body>

</html>
```

**输出:**

![](img/b60359ac4b900391c33dacf7b4a18099.png)