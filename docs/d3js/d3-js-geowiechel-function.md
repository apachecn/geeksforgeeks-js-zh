# D3.js geoWiechel()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-geowiechel-function/](https://www.geeksforgeeks.org/d3-js-geowiechel-function/)

D3.js 是一个 JavaScript 库，用于在 web 浏览器中产生动态的、交互式的数据可视化。它利用了可伸缩矢量图形、HTML5 和级联样式表标准。

d3.js 中的 **geoWiechel()函数**用于绘制 Wiechel 投影，这是一种方位角的等面积投影，也是威廉·h·Wiechel 在 1879 年提出的新奇地图。这也是一种改进的方位投影。方向、形状和距离的扭曲在边缘相当严重。

**语法:**

```
d3.geoWiechel()
```

**参数:**此方法不接受任何参数。

**返回值:**该方法根据给定的 JSON 数据创建并返回 Wiechel 投影。

**示例 1:** 以下示例对世界进行 Wiechel 投影，中心位于(0，0)且旋转为 0。

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

        // Wiechel projection
        // Center(0,0) with 0 rotation
        var gfg = d3.geoWiechel()
            .scale(width / 1.5 / Math.PI)
            .rotate([0,0])
            .center([0,0])
            .translate([width / 2, height / 2]);

        // Loading the JSON data
        d3.json("https://raw.githubusercontent.com/"
            +"janasayantan/datageojson/master/world.json", 
            function(data){
                // Draw the map
                svg.append("g")
                    .selectAll("path")
                    .data(data.features)
                    .enter().append("path")
                    .attr("fill", "DarkSlateGrey")
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

![](img/9d441e283c1cc65bda9ac5d59d6cb388.png)

世界的维切尔投影，无旋转，以(0，0)为中心

**示例 2:** 以下示例在自定义中心和旋转后，对世界进行维切尔投影。

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
    <div style="width:500px; height:600px;"> 
        <svg width="500" height="450"> 
        </svg> 
    </div> 

    <script>

        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // Wiechel  projection
        // Center(0,0) and -90 degree
        // rotation w.r.t X axis
        var gfg = d3.geoWiechel()
            .scale(width / 1.3 / Math.PI)
            .rotate([0,-90])
            .center([0,0])
            .translate([width / 2, height / 2])

        // Loading the json data
        d3.json("https://raw.githubusercontent.com/"
            +"janasayantan/datageojson/master/world.json", 
            function(data){
                // Draw the map
                svg.append("g")
                    .selectAll("path")
                    .data(data.features)
                    .enter().append("path")
                    .attr("fill", "DarkSlateBlue")
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

![](img/0522d4d757e1cf9296f287dbcac08567.png)

X 轴旋转-90 度并以(0，0)为中心的威奇投影