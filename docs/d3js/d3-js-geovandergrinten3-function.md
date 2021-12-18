# D3.js geoVanDerGrinten3()功能

> 原文:[https://www . geesforgeks . org/D3-js-geovandergrinten 3-function/](https://www.geeksforgeeks.org/d3-js-geovandergrinten3-function/)

D3.js 是一个 JavaScript 库，用于在 web 浏览器中产生动态的、交互式的数据可视化。它利用了可伸缩矢量图形、HTML5 和级联样式表标准。

d3.js 中的 **geoVanDerGrinten3()函数**用于绘制范德格林顿三世投影。

**语法:**

```
d3.geoVanDerGrinten3()

```

**参数:**此方法不接受任何参数。

**返回值:**该方法根据给定的 JSON 数据创建并返回 geoVanDerGrinten III 投影。

**示例 1:** 以下示例绘制了以(0，0)为中心，0°旋转的范德格林顿三世世界投影。

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

        // VanDerGrinten3 projection
        // Center(0,0) with 0 rotation
        var gfg = d3.geoVanDerGrinten3()
            .scale(width / 2.5 / Math.PI)
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
                    .attr("fill", "Black")
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

![](img/468e93e1fc0e7acd1a2b17e6119c7705.png)

范德格林 3 世界投影，无旋转，以(0，0)为中心

**示例 2:** 以下示例绘制了 VanDerGrinten III 改变中心和旋转后的世界投影。

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

        // VanDerGrinten3  projection
        // Center(10,10) and 45 degree rotation w.r.t Y axis
        var gfg = d3.geoVanDerGrinten3()
            .scale(width / 2.2 / Math.PI)
            .rotate([45,0])
            .center([10,10])
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

![](img/66e6a3f71c6b1e96f42b0c334ad5c11b.png)

范德格林登 3 投影，绕 Y 轴旋转 45 度，中心位于(10，10)