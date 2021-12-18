# D3.js geoArmadillo()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-geoarmadillo-function/](https://www.geeksforgeeks.org/d3-js-geoarmadillo-function/)

**d3.js** 中的**犰狳()**功能用于绘制给定 geojson 数据的**犰狳投影**。这是一种用于世界地图的地图投影，可以用来显示地球的大部分，而不是透视的有限视图。它既不共形也不等面积。默认情况下，中心假定平行度为 20，如果使用不同的平行度，则可以更改中心。

**语法:**

```
d3.geoArmadillo()
```

**参数:**此方法不接受任何参数。

**返回值:**该方法返回犰狳投影。

**示例 1:** 以下示例绘制了世界的犰狳投影。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script src=
        "https://d3js.org/d3.v4.js">
    </script>
    <script src=
"https://d3js.org/d3-geo-projection.v2.min.js">
    </script>
</head>

<body>
    <div style="width:700px; height:700px;">
        <center>
            <h3 style="color:green">
                Armadillo Projection of World
            </h3>
        </center>
        <svg width="700" height="350">
        </svg>
    </div>

    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // Armadillo projection
        var gfg = d3.geoArmadillo()
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
                    .attr("fill", "blue")
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

![](img/f014ab7d1515859ec2c7ab32c16b9b4a.png)

**示例 2:** 以下示例绘制了亚洲的犰狳投影。

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
    <div style="width:500px; height:700px;">
        <center>
            <h3 style="color:green">
                Armadillo Projection of Asia
            </h3>
        </center>
        <svg width="600" height="350">
        </svg>
    </div>
    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // Armadillo projection
        var gfg = d3.geoArmadillo()
            .scale(width / 1.5 / Math.PI)
            .center([100, 0])
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
                    .style("stroke", "#ffff");
            })
    </script>
</body>

</html>
```

**输出:**

![](img/61176a1cdb48e0056aff786abd64cb3b.png)