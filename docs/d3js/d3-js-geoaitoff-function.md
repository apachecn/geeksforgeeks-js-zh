# D3.js geoAitoff()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-geoaitoff-function/](https://www.geeksforgeeks.org/d3-js-geoaitoff-function/)

**d3.js** 中的 **geoAitoff()** 功能用于绘制给定 geojson 数据的 **Aitoff 投影**。这是一种改进的方位投影，其中经纬线网络采用椭圆的形式。

**语法:**

```
d3.geoAitoff()
```

**参数:**此方法不接受任何参数。

**返回:**该方法返回艾托夫投影。

**示例 1:** 以下示例绘制了亚洲的艾托夫投影。

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
    <div style="width:1000px; height:700px;">
        <center>
            <h4 style="color:green" font='bold'>
                geoAitoff Projection of Asia
            </h4>
        </center>
        <svg width="650" height="350">
        </svg>
    </div>

    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // geoAitoff projection
        var gfg = d3.geoAitoff()
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

![](img/e837ee4c8745774f8c22109a003fbaba.png)

**示例 2:** 以下示例绘制了世界的艾托夫投影。

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
    <div style="width:700px; height:700px;">
        <center>
            <h3 style="color:green" font='bold'>
                geoAitoff Projection of World
            </h3>
        </center>
        <svg width="700" height="500">
        </svg>
    </div>
    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // geoAitoff projection
        var gfg = d3.geoAitoff()
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

![](img/b600f549ac2ed5abc56908c620d980b3.png)