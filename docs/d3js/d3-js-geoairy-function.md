# D3.js geoAiry()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-geoairy-function/](https://www.geeksforgeeks.org/d3-js-geoairy-function/)

**d3.js** 中的 **geoAiry** ()函数用于从给定的 geojson 数据中绘制 **Airy 的最小误差方位投影**。这是由于地图投影中的最小化而导致的形状和面积误差的解决方案。

**语法:**

```
d3.geoAiry()

```

**参数:**此方法不接受任何参数。

**返回值:**该方法返回艾里的最小误差方位投影。

**示例 1:** 以下示例绘制了亚洲的艾里最小误差方位投影。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script src="https://d3js.org/d3.v4.min.js">
    </script>
    <script src=
"https://d3js.org/d3-geo-projection.v2.min.js">
    </script>
</head>

<body>
    <div style="width:1200px; height:1000px;">
        <center>
            <h3 style="color:green">
                geoAiry Projection of Asia
            </h3>
        </center>
        <svg width="800" height="500">
        </svg>
    </div>
    <svg width="400" height="300"></svg>
    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // geoAiry projection
        var gfg = d3.geoAiry()
            .scale(width / 1.5 / Math.PI)
            .translate([width / 2, height / 2]);

        // Loading the json data
        d3.json("https://raw.githubusercontent.com/" +
            "janasayantan/datageojson/master/" +
            "geoasia.json",
            function (data) {

                // Draw the map
                svg.append("g")
                    .selectAll("path")
                    .data(data.features)
                    .enter().append("path")
                    .attr("fill", "black")
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

![](img/c6cfcc2018e946ff2c20e967f3e52ebf.png)

**示例 2:** 以下示例绘制了世界的艾里最小误差方位投影。

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
        <center>
            <h3 style="color:grey">
                azimuthal Projection of World
            </h3>
        </center>
        <svg width="700" height="550">
        </svg>
    </div>
    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // geoAiry projection
        var gfg = d3.geoAiry()
            .scale(width / 1.5 / Math.PI)
            .translate([width / 2, height / 2]);

        // Loading the json data
        d3.json("https://raw.githubusercontent.com/" +
            "janasayantan/datageojson/master/" +
            "geoworld%20.json",
            function (data) {

                // Draw the map
                svg.append("g")
                    .selectAll("path")
                    .data(data.features)
                    .enter().append("path")
                    .attr("fill", "green")
                    .attr("d", d3.geoPath()
                        .projection(gfg)
                    )
                    .style("stroke", "#ffff");
            });
    </script>
</body>

</html>
```

**输出:**

![](img/5388c9c0cc50b94e4e99e0e442558896.png)