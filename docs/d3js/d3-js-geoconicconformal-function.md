# D3 . js geoconiconformal()函数

> 原文:[https://www . geeksforgeeks . org/D3-js-geoconiconformal-function/](https://www.geeksforgeeks.org/d3-js-geoconicconformal-function/)

D3.js 是一个 JavaScript 库，用于在 web 浏览器中产生动态的、交互式的数据可视化。它利用了可伸缩矢量图形、HTML5 和级联样式表标准。d3.js 中的**geoconiconformal**()函数用于绘制 Lambert 共形圆锥投影。

**语法:**

```
d3.geoConicConformal()
```

**参数**:此方法不接受任何参数。

**返回值:**该方法根据给定的 json 数据创建一个 Lambert 共形圆锥投影。

**示例:**以下示例对世界进行共形圆锥投影，中心在(0，0)且无旋转。

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
    <div style="width:600px; height:900px;">
        <center>
            <h3 style="color:black">
            </h3>
        </center>

        <svg width="400" height="500">
        </svg>
    </div>

    <script>

        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // ConicConformal projection
        // Center(0, 0) with 0 rotation
        var gfg = d3.geoConicConformal()
            .scale(width / 1.5 / Math.PI)
            .rotate([0, 0])
            .center([0, 0])
            .translate([width / 2, height / 2])

        // Loading the json data
        // Used json file stored at 
        // https://raw.githubusercontent.com/janasayantan
        // /datageojson/master/world.json

        var myURL = "https://raw.githubusercontent.com/"
            + "janasayantan" +
            "/datageojson/master/world.json"

        d3.json(myURL, function (data) {

            // Draw the map
            svg.append("g")
                .selectAll("path")
                .data(data.features)
                .enter().append("path")
                .attr("fill", "DarkGoldenRod")
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

![](img/1ec6bb93261da9a1142f30aabb83d131.png)

**共形圆锥投影，无旋转，以(0，0)** 为中心