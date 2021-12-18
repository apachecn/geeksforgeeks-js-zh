# D3.js geoBaker()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-geobaker-function/](https://www.geeksforgeeks.org/d3-js-geobaker-function/)

**d3.js** 中的 **geoBaker()** 功能用于根据给定的 geojson 数据绘制 **Baker Dinomic 投影**。

**语法:**

```
d3.geoBaker()

```

**参数:**此方法不接受任何参数。

**返回:**该方法返回贝克地诺麦投影。

**示例:**以下示例制作了世界的 Baker Dinomic 投影。

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
    <div style="width:800px; height:600px;">
        <center>
            <h3 style="color:red">
                Baker Dinomic Projection of World
            </h3>
        </center>
        <svg width="700" height="550">
        </svg>
    </div>
    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // Baker Dinomic projection
        var gfg = d3.geoBaker()
            .scale(width / 1.5 / Math.PI)
            .translate([width / 2, height / 2])

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

![](img/8debf7c4ae58f410a5505be16cff64f3.png)