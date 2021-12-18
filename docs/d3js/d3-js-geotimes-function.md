# D3.js geoTimes()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-geotimes-function/](https://www.geeksforgeeks.org/d3-js-geotimes-function/)

D3.js 是一个 JavaScript 库，用于在 web 浏览器中产生动态的、交互式的数据可视化。它利用了可伸缩矢量图形、HTML5 和级联样式表标准。

d3.js 中的 **geoTimes()函数**用于绘制约翰·缪尔时报投影。

**语法:**

```
d3.geoTimes()
```

**参数:**此方法不接受任何参数。

**返回值:**该方法根据给定的 JSON 数据创建并返回约翰·缪尔时报投影。

**示例 1:** 以下示例绘制了以(0，0)为中心，0°旋转的世界的时间投影。

## 超文本标记语言

```
<!DOCTYPE html> 
<html lang="en"> 

<head> 
    <meta charset="UTF-8" /> 
    <meta name="viewport"
        content="width=device-width, 
                initial-scale=1.0"/> 

    <script src=
        "https://d3js.org/d3.v4.js">
    </script>
    <script src=
"https://d3js.org/d3-geo-projection.v2.min.js">
    </script>
</head>

<body> 
    <div style="width:700px; height:500px;"> 
        <svg width="600" height="450"> 
        </svg> 
    </div> 

    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // Times projection
        // Center(0,0) with 0 rotation
        var gfg = d3.geoTimes()
            .scale(width / 1.5 / Math.PI)
            .rotate([0,0])
            .center([0,0])
            .translate([width / 2, height / 2])

        // Loading the json data
        d3.json("https://raw.githubusercontent.com/"
        + "janasayantan/datageojson/master/world.json", 
        function(data){
            // Drawing the map
            svg.append("g")
                .selectAll("path")
                .data(data.features)
                .enter().append("path")
                    .attr("fill", "BLACK")
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

![](img/d55cb93237d154271d8096ff0d78e88c.png)

没有旋转且以(0，0)为中心的世界的时间投影

**示例 2:** 以下示例绘制了改变中心和旋转后世界的时间投影。

## 超文本标记语言

```
<!DOCTYPE html> 
<html lang="en"> 

<head> 
    <meta charset="UTF-8" /> 
    <meta name="viewport"
        content="width=device-width, 
                initial-scale=1.0"/> 

    <script src=
        "https://d3js.org/d3.v4.js">
    </script>
    <script src=
"https://d3js.org/d3-geo-projection.v2.min.js">
    </script>
</head> 

<body> 
    <div style="width:700px; height:600px;"> 
        <svg width="500" height="450"> 
        </svg> 
    </div> 

    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // Times  projection
        // Center(-10,0) and 90 degree
        // rotation w.r.t Y axis
        var gfg = d3.geoTimes()
            .scale(width / 1.8 / Math.PI)
            .rotate([90,0])
            .center([-10,0])
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
                    .attr("fill", "grey")
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

![](img/ff8c974328a0a7d7f85b7b08c032e2e8.png)

相对于 Y 轴旋转 90 度并以(-10，0)为中心的时间投影