# D3.js geoHammer()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-geohammer-function/](https://www.geeksforgeeks.org/d3-js-geohammer-function/)

D3.js 是一个 JavaScript 库，用于在 web 浏览器中产生动态的、交互式的数据可视化。它利用了可伸缩矢量图形、HTML5 和级联样式表标准。

d3.js 中的 **geoHammer()函数**用于绘制 Hammer 投影，是 Ernst Hammer 描述的等面积地图投影。

**语法:**

```
d3.geoHammer()

```

**参数:**此方法不接受任何参数。

**返回值:**这个方法从给定的 JSON 数据创建并返回一个锤子投影。

**例 1:** 下面的例子画出了世界的锤子投影，中心在(0，0)，旋转 0。

## 超文本标记语言

```
<!DOCTYPE html> 
<html lang="en"> 

<head> 
    <meta charset="UTF-8" /> 
    <meta name="viewport"
        content="width=device-width, 
                initial-scale=1.0"/> 

    <script src="https://d3js.org/d3.v4.js"></script>

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

        // Hammer projection
        // Center(0,0) with 0 rotation
        var gfg = d3.geoHammer()
            .scale(width / 1.5 / Math.PI)
            .rotate([0,0])
            .center([0,0])
            .translate([width / 2, height / 2])

        // Loading the json data
        d3.json(
            "https://raw.githubusercontent.com/"
            +"janasayantan/datageojson/master/world.json", 
                function(data){
                // Drawing the map
                svg.append("g")
                    .selectAll("path")
                    .data(data.features)
                    .enter().append("path")
                    .attr("fill", "SlateGray")
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

![](img/13b7a5f7ff6f4ddcee1186dbc2c70f2b.png)

世界的锤子投影，无旋转，以(0，0)为中心

**示例 2:** 以下示例在自定义中心和旋转后绘制世界的锤子投影。

## 超文本标记语言

```
<!DOCTYPE html> 
<html lang="en"> 

<head> 
    <meta charset="UTF-8" /> 
    <meta name="viewport"
        content="width=device-width, 
                initial-scale=1.0"/> 

    <script src="https://d3js.org/d3.v4.js"></script>

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

        // Hammer  projection
        // Center(0,0) and 90 degree rotation w.r.t Y axis
        var gfg = d3.geoHammer()
            .scale(width / 1.3 / Math.PI)
            .rotate([90,0])
            .center([0,0])
            .translate([width / 2, height / 2])

        // Loading the json data
        d3.json(
            "https://raw.githubusercontent.com/"
            +"janasayantan/datageojson/master/world.json", 
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

![](img/29dffc18732e2ca443a3314dee2e734a.png)

锤子投影，相对于 Y 轴旋转 90 度，中心位于(0，0)