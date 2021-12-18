# D3.js geoVanDerGrinten2()功能

> 原文:[https://www . geesforgeks . org/D3-js-geovandergrinten 2-function/](https://www.geeksforgeeks.org/d3-js-geovandergrinten2-function/)

D3.js 是一个 JavaScript 库，用于在 web 浏览器中产生动态的、交互式的数据可视化。它利用了可伸缩矢量图形、HTML5 和级联样式表标准。

d3.js 中的 **geoVanDerGrinten2()函数**用于绘制范德格林顿 II 投影。

**语法:**

```
d3.geoVanDerGrinten2()
```

**参数:**此方法不接受任何参数。

**返回值:**该方法根据给定的 JSON 数据创建 geoVanDerGrinten II 投影。

**示例 1:** 以下示例绘制了以(0，0)为中心，0°旋转的范德格林顿 II 世界投影。

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
        <svg width="700" height="400"> 
        </svg> 
    </div> 

    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // VanDerGrinten2  projection
        // Center(0,0) and 0 rotation 
        var gfg = d3.geoVanDerGrinten2()
            .scale(width / 3.0 / Math.PI)
            .rotate([0,0])
            .center([0,0])
            .translate([width / 2, height / 2])

        // Loading the JSON data
        d3.json(
            "https://raw.githubusercontent.com/"+
            "janasayantan/datageojson/master/world.json", 
            function(data){
                // Draw the map
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

![](img/ac973148c0b2a572de2a7f6f199f3fb3.png)

无旋转且以(0，0)为中心的世界的范德普林 2 投影

**示例 2:** 以下示例绘制了范德格林顿 II 在改变中心和旋转后对世界的投影。

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
        <svg width="700" height="400"> 
        </svg> 
    </div> 

    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // VanDerGrinten2  projection
        // Center(10,10) and 45 degree rotation w.r.t  Y axis
        var gfg = d3.geoVanDerGrinten2()
            .scale(width / 3.0 / Math.PI)
            .rotate([45,0])
            .center([10,10])
            .translate([width / 2, height / 2])

        // Loading the JSON data
        d3.json(
            "https://raw.githubusercontent.com/"+
            "janasayantan/datageojson/master/world.json", 
            function(data){
                // Draw the map
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

![](img/d314f70e7c1079ef1ba9bea8cb248471.png)

范德格林登 2 投影，绕 Y 轴旋转 45 度，中心位于(10，10)