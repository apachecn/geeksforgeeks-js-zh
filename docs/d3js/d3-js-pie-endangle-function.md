# D3.js pie.endAngle()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-pie-endangle-function/](https://www.geeksforgeeks.org/d3-js-pie-endangle-function/)

**D3.js** 中的**馅饼. endAngle()功能**用于设置馅饼的结束角度。当指定角度时，它将结束角度设置为给定的角度或函数，并返回饼图生成器。如果未指定角度，它将返回当前的结束角度访问器，默认为无结束角度。

**语法:**

```
pie.endAngle( angle )
```

**参数:**该函数接受一个参数，如上所述，如下所述。

*   **角度:**是以弧度为单位指定终点角度的数字或函数。这是一个可选参数。

**返回值:**这个函数不返回任何东西。

下面给出了几个 D3.js 中 **pie.endAngle()** 函数的例子；

**例 1:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script src="https://d3js.org/d3.v6.min.js">
    </script>
</head>

<body>
    <div style="width:300px; height:300px;">
        <center>
            <h1 style="color:green">
                GeeksforGeeks
            </h1>
            <h2>
                pie.endAngle()
            </h2>
        </center>
        <svg width="300" height="250">
        </svg>
    </div>

    <script>
        // Data to be added in the pie chart
        var data = [
            { "property": "p5", "value": 19 },
            { "property": "p5", "value": 12 },
            { "property": "p4", "value": 11 },
            { "property": "p3", "value": 10 },
            { "property": "p2", "value": 9 },
        ]

        // Selecting SVG using d3.select()
        var svg = d3.select("svg");

        // Creating Pie generator
        var pie = d3.pie()
            .value((d) => { return d.value })
            .startAngle(3)
            // Use of pie.endAngle() Function
            .endAngle(1)
            (data);
        // Creating arc
        var arc = d3.arc()
            .innerRadius(0)
            .outerRadius(80);

        let g = svg.append("g")
            .attr("transform", "translate(150,120)");

        // Grouping different arcs
        var arcs = g.selectAll("arc")
            .data(pie)
            .enter()
            .append("g");

        // Appending path
        arcs.append("path")
            .attr("fill", (data, i) => {
                return d3.schemeSet3[i];
            })
            .attr("d", arc);
    </script>
</body>

</html>
```

**输出:**

![](img/4e79d74de51cfd0b3f1f0b5b7e25dadb.png)

**例 2:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script src="https://d3js.org/d3.v6.min.js">
    </script>
</head>

<body>
    <div style="width:300px; height:300px;">
        <center>
            <h1 style="color:green">
                GeeksforGeeks
            </h1>
            <h2>
                pie.endAngle()
            </h2>
        </center>
        <svg width="300" height="250">
        </svg>
    </div>
    <script>
        // Data to be added in the pie chart
        var data = [
            { "property": "p5", "value": 19 },
            { "property": "p5", "value": 12 },
            { "property": "p4", "value": 11 },
            { "property": "p3", "value": 10 },
            { "property": "p2", "value": 9 },
            { "property": "p5", "value": 19 },
            { "property": "p5", "value": 12 },
            { "property": "p4", "value": 11 },
            { "property": "p3", "value": 10 },
            { "property": "p2", "value": 9 },
        ]

        // Selecting SVG using d3.select()
        var svg = d3.select("svg");

        // Creating Pie generator
        var pie = d3.pie()
            .value((d) => { return d.value })
            // Use of pie.endAngle() Function
            .endAngle(4)
            (data);
        // Creating arc
        var arc = d3.arc()
            .innerRadius(10)
            .outerRadius(80);

        let g = svg.append("g")
            .attr("transform", "translate(150,120)");

        // Grouping different arcs
        var arcs = g.selectAll("arc")
            .data(pie)
            .enter()
            .append("g");

        // Appending path
        arcs.append("path")
            .attr("fill", (data, i) => {
                return d3.schemeSet3[i];
            })
            .attr("d", arc);
    </script>
</body>

</html>
```

**输出:**

![](img/bf8a970c3d5b31ffe4949ff572adbc16.png)