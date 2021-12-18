# D3.js curveBasis()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-curvebasis-method/](https://www.geeksforgeeks.org/d3-js-curvebasis-method/)

基础曲线插值器生成三次基础样条，其中提供给生成器的点被用作控制点。基于三次  样条曲线的直线中有一条曲线。

**语法:**

```
d3.curveBasis()

```

**参数:**该方法不取参数

**返回值:**此方法不返回任何内容。

**例 1:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<meta charset="utf-8">

<head>
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/d3/4.2.2/d3.min.js">
    </script>
</head>

<body>
    <h1 style="text-align:center; color:green;">
        GeeksforGeeks
    </h1>

    <center>
        <svg id="gfg" width="200" height="200"></svg>
    </center>

    <script>
        var data = [
            { x: 0, y: 0 },
            { x: 1, y: 3 },
            { x: 2, y: 15 },
            { x: 5, y: 15 },
            { x: 6, y: 1 },
            { x: 7, y: 5 },
            { x: 8, y: 1 }];

        var xScale = d3.scaleLinear()
            .domain([0, 8]).range([25, 175]);
        var yScale = d3.scaleLinear()
            .domain([0, 20]).range([175, 25]);

        var line = d3.line()
            .x((d) => xScale(d.x))
            .y((d) => yScale(d.y))
            // curveBasis is used
            .curve(d3.curveBasis);

        d3.select("#gfg")
            .append("path")
            .attr("d", line(data))
            .attr("fill", "none")
            .attr("stroke", "green");
    </script>
</body>

</html>
```

**输出:**

![](img/18cb5d54a732a9e6ddaa0d32f0f84455.png)

**例 2:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<meta charset="utf-8">

<head>
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/d3/4.2.2/d3.min.js">
    </script>
</head>

<body>
    <h1 style="text-align:center; color:green;">
        GeeksforGeeks
    </h1>

    <center>
        <svg id="gfg" width="200" height="200"></svg>
    </center>

    <script>
        var points = [
            { xpoint: 25, ypoint: 150 },
            { xpoint: 75, ypoint: 85 },
            { xpoint: 100, ypoint: 115 },
            { xpoint: 175, ypoint: 25 }];

        var Gen = d3.line()
            .x((p) => p.xpoint)
            .y((p) => p.ypoint)
            .curve(d3.curveBasis);

        d3.select("#gfg")
            .append("path")
            .attr("d", Gen(points))
            .attr("fill", "none")
            .attr("stroke", "green");
    </script>
</body>

</html>
```

**输出:**

![](img/d4b8a41b5414c3976b160fe7a091bc42.png)