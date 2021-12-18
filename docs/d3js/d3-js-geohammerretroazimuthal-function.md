# D3 . js geohammersretroyaltional()函数

> 原文:[https://www . geeksforgeeks . org/D3-js-geohammererchazed-function/](https://www.geeksforgeeks.org/d3-js-geohammerretroazimuthal-function/)

D3.js 是一个 JavaScript 库，用于在 web 浏览器中产生动态的、交互式的数据可视化。它利用了可伸缩矢量图形、HTML5 和级联样式表标准。d3.js 中的**地球锤回方位**()函数用于绘制锤回方位投影。

**语法:**

```
d3.geoHammerRetroazimuthal()
```

**参数:**此方法不接受任何参数。

**返回值:**该方法根据给定的 json 数据创建世界的 HammerRetroazimuthal 投影。

**示例 1:** 下面的示例绘制了世界的哈默回方位投影，中心位于(0，0)和 0°旋转。

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, 
        initial-scale=1.0" />
</head>

<body>
    <div style="width:700px; height:500px;">
        <center>
            <h3 style="color:black">
            </h3>
        </center>
        <svg width="600" height="450">
        </svg>
    </div>
    <script src="https://d3js.org/d3.v4.js"></script>
    <script src=
    "https://d3js.org/d3-geo-projection.v2.min.js">
    </script>
    <script>

        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // HammerRetroazimuthal projection
        // Center(0, 0) with 0 rotation
        var gfg = d3.geoHammerRetroazimuthal()
            .scale(width / 3.8 / Math.PI)
            .rotate([0, 0])
            .center([0, 0])
            .translate([width / 2, height / 2])

        // Loading the json data
        // Used json file stored at 
        /*https://raw.githubusercontent.com/janasayantan
        /datageojson/master/world.json*/
        d3.json("https://raw.githubusercontent.com/"
            + "janasayantan/datageojson/master/world.json",
            function (data) {

                // Drawing the map
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

![](img/3f20cef2535b1c622bc9b4f73ae00746.png)

世界的锤回方位角投影，无旋转，中心在(0，0)