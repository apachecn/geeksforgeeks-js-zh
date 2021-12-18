# D3.js geoConicEqualArea()函数

> 原文:[https://www . geesforgeks . org/D3-js-geoconicequalarea-function/](https://www.geeksforgeeks.org/d3-js-geoconicequalarea-function/)

**d3.js** 中的 **geoConicEqualArea()** 功能用于根据给定的 geojson 数据绘制**艾伯斯的圆锥等面积** **投影**。

**语法:**

```
d3.geoConicEqualArea()

```

**参数:**此方法不接受任何参数。

**返回值:**此方法返回圆锥等面积投影。

**示例 1:** 以下示例绘制世界的圆锥等面积投影，中心位于(0，0)，旋转 0 度。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script src="https://d3js.org/d3.v4.js">
    </script>
    <script src=
"https://d3js.org/d3-geo-projection.v2.min.js">
    </script>
</head>

<body>
    <div style="width:700px; height:500px;">
        <svg width="600" height="450"></svg>
    </div>

    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // ConicEqualArea projection with
        // Center at (0, 0) with rotation
        // of 0 degrees 
        var gfg = d3.geoConicEqualArea()
            .scale(width / 1.8 / Math.PI)
            .rotate([0, 0])
            .center([0, 0])
            .translate([width / 2, height / 2]);

        // Loading the json data
        d3.json("https://raw.githubusercontent.com/" +
            "janasayantan/datageojson/master/" +
            "world.json",
            function (data) {

                // Drawing the map
                svg.append("g")
                    .selectAll("path")
                    .data(data.features)
                    .enter().append("path")
                    .attr("fill", "Black")
                    .attr("d", d3.geoPath()
                        .projection(gfg)
                    )
                    .style("stroke", "#ffff")
            });
    </script>
</body>

</html>
```

**输出:**

![](img/004bba0878acc4d65c35a2649438d964.png)

**示例 2:** 以下示例绘制世界的圆锥等面积投影，中心位于(-10，0)，相对于 y 轴旋转 90 度。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script src="https://d3js.org/d3.v4.js">
    </script>
    <script src=
"https://d3js.org/d3-geo-projection.v2.min.js">
    </script>
</head>

<body>
    <div style="width:700px; height:600px;">
        <svg width="500" height="450"></svg>
    </div>

    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // ConicEqualArea  projection
        // Center at (-10,0) and 90 degree
        // rotation w.r.t y-axis
        var gfg = d3.geoConicEqualArea()
            .scale(width / 1.8 / Math.PI)
            .rotate([90, 0])
            .center([-10, 0])
            .translate([width / 2, height / 2]);

        // Loading the json data
        d3.json("https://raw.githubusercontent.com/" +
            "janasayantan/datageojson/master/" +
            "world.json",
            function (data) {

                // Draw the map
                svg.append("g")
                    .selectAll("path")
                    .data(data.features)
                    .enter().append("path")
                    .attr("fill", "grey")
                    .attr("d", d3.geoPath()
                        .projection(gfg)
                    )
                    .style("stroke", "#ffff")
            });
    </script>
</body>

</html>
```

**输出:**

![](img/49f2311a74be556fd4e5aaa3f5658c6c.png)