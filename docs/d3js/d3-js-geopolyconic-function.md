# D3.js 地缘政治()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-geopolyconic-function/](https://www.geeksforgeeks.org/d3-js-geopolyconic-function/)

JavaScript **D3.js** 库使用 HTML5、可缩放矢量图形和级联样式表为网页提供交互式数据可视化。
使用 **d3.js** 中的**地缘坐标**()功能绘制**美国多坐标**投影。

**语法:**

```
d3.geoPolyconic()
```

**参数:**此方法不接受任何参数。

**返回值:**该方法根据给定的 JSON 数据创建美国多点投影。

**示例 1:** 以下示例创建世界的多曲面投影，中心位于(0，0)且无旋转。

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, 
                initial-scale=1.0" />
</head>

<body>
    <div style="width: 700px;
                    height: 500px;">
        <center>
            <h3 style="color: black;"></h3>
        </center>

        <svg width="600" height="450"></svg>
    </div>
    <script src="https://d3js.org/d3.v4.js"></script>
    <script src=
    "https://d3js.org/d3-geo-projection.v2.min.js">
    </script>
    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // Polyconic projection
        // Center(0, 0) with 0 rotation
        var gfg = d3
            .geoPolyconic()
            .scale(width / 2.0 / Math.PI)
            .rotate([0, 0])
            .center([0, 0])
            .translate([width / 2, height / 2]);

        // Loading the json data
        // Used json file stored at 
        /*https://raw.githubusercontent.com/janasayantan
                    /datageojson/master/world.json*/
        d3.json("https://raw.githubusercontent.com/"
            + "janasayantan/datageojson/master/world.json",
            function (data) {
                // Drawing the map
                svg.append("g").selectAll("path")
                    .data(data.features).enter().append("path")
                    .attr("fill", "SeaGreen")
                    .attr("d", d3.geoPath().projection(gfg))
                    .style("stroke", "#ffff");
            });
    </script>
</body>

</html>
```

**输出:**

![](img/a6b1ff93d90b6f1135de6ab87a0d77a2.png)

**示例 2:** 在下面的示例中，我们将创建世界的多曲面投影，中心位于(0，-20)并相对于 Y 轴旋转 90 度。

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, 
                initial-scale=1.0" />
</head>

<body>
    <div style="width: 700px; height: 600px;">
        <center>
            <h3 style="color: black;"></h3>
        </center>

        <svg width="500" height="450"></svg>
    </div>
    <script src="https://d3js.org/d3.v4.js"></script>
    <script src=
    "https://d3js.org/d3-geo-projection.v2.min.js">
    </script>
    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // Polyconic  projection
        // Center(0, -20) and 90 degree
        // rotation w.r.t Y axis
        var gfg = d3
            .geoPolyconic()
            .scale(width / 2.0 / Math.PI)
            .rotate([90, 0])
            .center([0, -20])
            .translate([width / 2, height / 2]);

        // Loading the json data
        // Used json file stored at 
        /*https://raw.githubusercontent.com/janasayantan
                    /datageojson/master/world.json*/
        d3.json("https://raw.githubusercontent.com/"
            + "janasayantan/datageojson/master/world.json",
            function (data) {
                // Draw the map
                svg.append("g").selectAll("path")
                    .data(data.features).enter()
                    .append("path").attr("fill", "SlateBlue")
                    .attr("d", d3.geoPath().projection(gfg))
                    .style("stroke", "#ffff");
            });
    </script>
</body>

</html>
```

**输出:**

![](img/a8ff62079d6b715fe555f4a539149f08.png)