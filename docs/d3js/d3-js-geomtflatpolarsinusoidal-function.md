# D3 . js geomtflatparlistic()函数

> 原文:[https://www . geeksforgeeks . org/D3-js-geomtflattpolarsinic-function/](https://www.geeksforgeeks.org/d3-js-geomtflatpolarsinusoidal-function/)

JavaScript **D3.js** 库使用 HTML5、可缩放矢量图形和级联样式表为网页提供交互式数据可视化。
使用 **d3.js** 中的**大地平极正弦**()功能绘制麦克布赖德–托马斯平极正弦等面积投影。

**语法:**

```
d3.geoMtFlatPolarSinusoidal()
```

**参数:**此方法不接受任何参数。

**返回值:**该方法根据给定的 JSON 数据创建 McBryde-Thomas 平极正弦等面积投影。

**示例 1:** 以下示例创建世界的 MtFlatPolarSinusoidal 投影，中心位于(0，0)且无旋转。

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content=
        "width=device-width, initial-scale=1.0" />
    <script src="https://d3js.org/d3.v4.js"></script>
    <script src=
"https://d3js.org/d3-geo-projection.v2.min.js">
    </script>
</head>

<body>
    <div style="width:700px; height:500px;">
        <svg width="600" height="450"></svg>
    </div>

    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // MtFlatPolarSinusoidal projection
        // Center(0,0) with 0 rotation
        var gfg = d3.geoMtFlatPolarSinusoidal()
            .scale(width / 1.8 / Math.PI)
            .rotate([0, 0])
            .center([0, 0])
            .translate([width / 2, height / 2])

        // Loading the json data
        // Used json file stored at 
        // https://raw.githubusercontent.com/janasayantan
        // /datageojson/master/world.json
        d3.json("https://raw.githubusercontent.com/"
            + "janasayantan/datageojson/master/world.json",
            function (data) {

                // Drawing the map
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

![](img/7479a5f6a76f25b406130b4f2618f03c.png)

**示例 2:** 在下面的示例中，我们将创建世界的 MtFlatPolarSinusoidal 投影，中心位于(0，10)并相对于 Y 轴旋转 60 度。

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content=
        "width=device-width, initial-scale=1.0" />
    <script src="https://d3js.org/d3.v4.js"></script>
    <script src=
"https://d3js.org/d3-geo-projection.v2.min.js">
    </script>
</head>

<body>
    <div style="width:700px; height:600px;">
        <svg width="500" height="450"></svg>
    </div>

    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // MtFlatPolarSinusoidal  projection
        // Center(0,10) and 60 degree
        // rotation w.r.t Y axis
        var gfg = d3.geoMtFlatPolarSinusoidal()
            .scale(width / 1.7 / Math.PI)
            .rotate([60, 0])
            .center([0, 10])
            .translate([width / 2, height / 2])

        // Loading the json data
        // Used json file stored at 
        // https://raw.githubusercontent.com/janasayantan
        // /datageojson/master/world.json
        d3.json("https://raw.githubusercontent.com/"
            + "janasayantan/datageojson/master/world.json",
            function (data) {

                // Draw the map
                svg.append("g")
                    .selectAll("path")
                    .data(data.features)
                    .enter().append("path")
                    .attr("fill", "GoldenRod")
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

![](img/6e3a42688cad608bdc528dd9bcd7416b.png)