# D3.js geoWagner4()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-geowagner4-function/](https://www.geeksforgeeks.org/d3-js-geowagner4-function/)

D3.js 是一个 JavaScript 库，用于在 web 浏览器中产生动态的、交互式的数据可视化。它利用了可伸缩矢量图形、HTML5 和级联样式表标准。

d3.js 中的 **geoWagner4()函数**用于绘制 Wagner IV 投影，也称为 Putniṇš P2。

**语法:**

```
d3.geoWagner4()
```

**参数:**此方法不接受任何参数。

**返回:**这个方法从给定的 JSON 数据创建并返回 Wagner4 投影。

**示例 1:** 以下示例绘制了世界的 Wagner4 投影，中心位于(0，0)且旋转为 0。

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

        // Wagner4 projection
        // Center(0,0) with 0 rotation
        var gfg = d3.geoWagner4()
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

![](img/28c09075990ec61af7685f512109dd2a.png)

Wagner4 世界投影，无旋转，以(0，0)为中心

**示例 2:** 以下示例绘制了改变中心和旋转后的 Wagner4 世界投影。

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

        // Wagner4  projection
        // Center(-10,0) and 90 degree
        // rotation w.r.t Y axis
        var gfg = d3.geoWagner4()
            .scale(width / 1.3 / Math.PI)
            .rotate([-90,0])
            .center([-10,0])
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

![](img/8bff4088d94ca2eab819ce72c0b3ebfe.png)

w . r . t . Y 轴旋转 90 度并以(-10，0)为中心的 Wagner4 投影