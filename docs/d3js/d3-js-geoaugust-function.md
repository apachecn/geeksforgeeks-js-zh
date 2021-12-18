# D3.js geoAugust()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-geoaugust-function/](https://www.geeksforgeeks.org/d3-js-geoaugust-function/)

**d3.js** 中的 **geoAugust** ()函数用于绘制给定 geojson 数据的 **August 的外摆线共形投影**。

**语法:**

```
d3.geoAugust()

```

**参数:**此方法不接受任何参数。

**返回:**此方法返回八月的外摆线共形投影。

**例 1:** 下面的例子绘制了八月的亚洲外摆线共形投影。

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
    <div style="width:800px; height:400px;">
        <center>
            <h4 style="color:green">
                August Projection of Asia
            </h4>
        </center>
        <svg width="500" height="300">
        </svg>
    </div>
    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // August projection
        var gfg = d3.geoAugust()
            .scale(width / 1.5 / Math.PI)
            .translate([width / 2, height / 2]);

        // Loading the geojson data 
        d3.json("https://raw.githubusercontent.com/" +
            "janasayantan/datageojson/master/" +
            "geoasia.json",
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

![](img/7833f86c3662125283f90769f2ace15c.png)

**例 2:** 下面的例子画出了八月的外摆线对世界的共形投影。

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
    <div style="width:700px; height:550px;">
        <center>
            <h3 style="color:green">
                August Projection of World
            </h3>
        </center>
        <svg width="700" height="550">
        </svg>
    </div>
    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // August projection
        var gfg = d3.geoAugust()
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

![](img/a886269a18589685a07e7e6c33c18587.png)