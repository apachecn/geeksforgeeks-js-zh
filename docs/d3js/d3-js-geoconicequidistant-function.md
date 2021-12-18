# D3.js 地理坐标魁地奇()功能

> 原文:[https://www . geesforgeks . org/D3-js-geoconicequidistant-function/](https://www.geeksforgeeks.org/d3-js-geoconicequidistant-function/)

**d3.js** 中的**地理坐标坐标**()功能用于根据给定的地理坐标数据绘制**圆锥等距投影**。

**语法:**

```
d3.geoConicEquidistant()

```

**参数:**此方法不接受任何参数。

**返回值:**该方法返回圆锥等距投影。

**示例 1:** 以下示例绘制世界的圆锥等距投影，中心位于(0，0)，旋转 0 度。

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

        // ConicEquidistant projection
        // with center at (0, 0) and
        // rotation of 0 degrees
        var gfg = d3.geoConicEquidistant()
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

![](img/47183ab66bcea74ba21e46a481b3d39d.png)

**示例 2:** 以下示例绘制世界的圆锥等距投影，中心位于(-10，0)，相对于 y 轴旋转 90 度。

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

        // ConicEquidistant projection
        // center at (-10,0) and 90 degrees
        // rotation w.r.t y-axis
        var gfg = d3.geoConicEquidistant()
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

![](img/5d7d10b2f32b8d1e5876d70d6099e320.png)