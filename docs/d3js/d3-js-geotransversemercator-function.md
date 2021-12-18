# D3.js geoTransverseMercator()功能

> 原文:[https://www . geeksforgeeks . org/D3-js-geotransversemercator-function/](https://www.geeksforgeeks.org/d3-js-geotransversemercator-function/)

D3.js 是一个 JavaScript 库，用于在 web 浏览器中产生动态的、交互式的数据可视化。它利用了可伸缩矢量图形、HTML5 和级联样式表标准。

d3.js 中的 **geoTransverseMercator()函数**用于绘制横向球面墨卡托投影。

**语法:**

```
d3.geoTransverseMercator()
```

**参数:**此方法不接受任何参数。

**返回值:**该方法根据给定的 JSON 数据创建一个横向墨卡托投影。

**示例:**下面的示例绘制了世界的横向墨卡托投影，中心位于(0，0)，旋转为 0。

## 超文本标记语言

```
<!DOCTYPE html> 
<html lang="en"> 

<head> 
    <meta charset="UTF-8" /> 
    <meta name="viewport"
        content="width=device-width, 
                initial-scale=1.0"/> 
</head> 

<body> 
    <div style="width:700px; height:600px;"> 
        <svg width="700" height="400"> 
        </svg> 
    </div> 

    <script src=
        "https://d3js.org/d3.v4.js">
    </script>
    <script src=
"https://d3js.org/d3-geo-projection.v2.min.js">
    </script>
    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // Transverse Mercator  projection
        // Center(0,0) and no rotation 
        var gfg = d3.geoTransverseMercator()
            .scale(width / 2.8 / Math.PI)
            .rotate([0,0])
            .center([0,0])
            .translate([width / 2, height / 2])

        // Loading the json data
        d3.json("https://raw.githubusercontent.com/"
        + "janasayantan/datageojson/master/world.json",
        function(data){

            // Draw the map
            svg.append("g")
                .selectAll("path")
                .data(data.features)
                .enter().append("path")
                    .attr("fill", "SaddleBrown")
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

![](img/fbeaeee4e0db7552f55c1a32b5921057.png)