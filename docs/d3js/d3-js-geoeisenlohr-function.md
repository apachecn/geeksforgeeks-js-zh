# D3.js geoEisenlohr()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-geoeisenlohr-function/](https://www.geeksforgeeks.org/d3-js-geoeisenlohr-function/)

JavaScript **D3.js** 库使用 HTML5、可缩放矢量图形和级联样式表为网页提供交互式数据可视化。 **d3.js** 中的 **geoEisenlohr** ()功能用于绘制 **Eisenlohr** 共形投影。

**语法:**

```
d3.geoEisenlohr()
```

**参数:**此方法不接受任何参数。

**返回:**该方法根据给定的 JSON 数据创建 Eisenlohr 投影。

**示例 1:** 以下示例创建世界的艾森洛投影，中心位于(0，0)且无旋转。

## 超文本标记语言

```

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, 
                initial-scale=1.0" />
    <script src="https://d3js.org/d3.v4.js"></script>
    <script src=
"https://d3js.org/d3-geo-projection.v2.min.js">
    </script>
</head>

<body>
    <div style="width:700px; height:600px;">
        <svg width="700" height="550">
        </svg>
    </div>

    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // Eisenlohr  projection
        // Center(0,0) and no rotation
        var gfg = d3.geoEisenlohr()
            .scale(width / 1.5 / Math.PI)
            .rotate([0, 0])
            .center([0, 0])
            .translate([width / 2, height / 2])

        // Loading the json data
        // Used json file stored at 
        // https://raw.githubusercontent.com/janasayantan
        // datageojson/master/world.json
        d3.json("https://raw.githubusercontent.com/"
            + "janasayantan/datageojson/master/world.json",
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
            })
    </script>

</html>
```

**输出:**

![](img/8d013b5b51d0fbdccbe507d4b4749928.png)

**示例 2:** 在下面的示例中，我们将创建以(30，0)为中心并相对于 Y 轴逆时针旋转 30 度的 Eckert5 世界投影。

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, 
                initial-scale=1.0" />
    <script src="https://d3js.org/d3.v4.js"></script>
    <script src=
"https://d3js.org/d3-geo-projection.v2.min.js">
    </script>
</head>

<body>
    <div style="width:700px; height:600px;">
        <svg width="700" height="550">
        </svg>
    </div>

    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // Eisenlohr  projection
        // Center(30, 0) and 30 degree rotation
        var gfg = d3.geoEisenlohr()
            .scale(width / 1.5 / Math.PI)
            .rotate([-30, 0])
            .center([30, 0])
            .translate([width / 2, height / 2])

        // Loading the json data
        // Used json file stored at 
        // https://raw.githubusercontent.com/janasayantan
        // /datageojson/master/world.json
        d3.json("https://raw.githubusercontent.com/"
            + "janasayantan/datageojson/master/world.json",
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
            })
    </script>
</body>

</html>
```

**输出:**

![](img/bb8e45f79e4ae67281d7ced0b963f55e.png)