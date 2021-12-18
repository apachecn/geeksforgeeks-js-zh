# D3.js geoCollignon()功能

> 哎哎哎:# t0]https://www . geeksforgeeks . org/D3-js-geoollignon-function/

JavaScript 库 **D3.js** 使用 HTML5、可伸缩矢量图形和级联样式表为网页提供交互式数据可视化。 **d3.js** 中的 **geoCollignon()** 功能用于绘制 Collignon 等面积伪圆柱投影。该投影用于 **HEALPix** 投影的极区。

**语法:**

```
d3.geoCollignon()
```

**参数:**此方法不接受任何参数。

**返回:**该方法根据给定的 JSON 数据创建一个 Collignon 投影。

**示例 1:** 以下示例进行世界的 Collignon 投影，中心在(0，0)，无旋转。

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

        // Collignon  projection
        // Center(0, 0) and no rotation
        var gfg = d3.geoCollignon()
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
                    .attr("fill", "BurlyWood")
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

![](img/2aa7dc2a08b7011900421e48db026c24.png)