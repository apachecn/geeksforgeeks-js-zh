# D3 . jsgeoequi 矩形()函数

> 原文:[https://www . geeksforgeeks . org/D3-js-geoequi 矩形-function/](https://www.geeksforgeeks.org/d3-js-geoequirectangular-function/)

D3.js 是一个 JavaScript 库，用于在 web 浏览器中产生动态的、交互式的数据可视化。它利用了可伸缩矢量图形、HTML5 和级联样式表标准。

d3.js 中的 geoequipmentalmatrix()函数用于绘制等矩形投影，这是一个简单的地图投影，归因于 Tyre 的 Marinus，托勒密声称他发明了投影。

**语法:**

```
d3.geoEquirectangular()
```

**参数:**此方法不接受任何参数。

**返回值:**这个方法从给定的 json 数据创建一个等矩形投影。

**示例 1:** 以下示例对世界进行等矩形投影，中心位于(0，0)，无旋转。

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, 
        initial-scale=1.0" />

    <script src="https://d3js.org/d3.v4.js">
    </script>
    <script src="https://d3js.org/d3-geo-projection.v2.min.js">
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

        // Equirectangular  projection
        // Center(0,0) and no rotation
        var gfg = d3.geoEquirectangular()
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

![](img/866fba646959587ed68e6d887f856663.png)

等矩形投影，无旋转，以(0，0)为中心

**示例 2:** 以下示例通过改变中心和旋转对世界进行等矩形投影。

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, 
                initial-scale=1.0" />
    <script src="https://d3js.org/d3.v4.js"></script>
    <script src="https://d3js.org/d3-geo-projection.v2.min.js"></script>
</head>

<body>
    <div style="width:700px; height:900px;">
        <svg width="400" height="450">
        </svg>
    </div>

    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // Equirectangular  projection
        // Center(0,10) and 45 degree 
        // anticlock rotation
        var gfg = d3.geoEquirectangular()
            .scale(width / 1.5 / Math.PI)
            .rotate([45, 0])
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

![](img/8eaa8d94bcb30c9b62d5d3c85e5c66b4.png)

**等矩形投影，反时针旋转 45 度，以(0，10)** 为中心