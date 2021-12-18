# D3.js geoBottomley()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-geobottomley-function/](https://www.geeksforgeeks.org/d3-js-geobottomley-function/)

D3.js 是一个 JavaScript 库，用于在 web 浏览器中产生动态的、交互式的数据可视化。它利用了可伸缩矢量图形、HTML5 和级联样式表标准。

d3.js 中的 **geoBottomley()函数**用于绘制 **Bottomley** 投影，该投影将纬度线绘制为同心圆弧，其弧长与它们在地球上的长度相等，并对称且等距地放置在垂直中心子午线上。

**语法:**

```
d3.geoBottomley()
```

**参数:**此方法不接受任何参数。

**返回值:**该方法根据给定的 JSON 数据创建一个 Bottomley 投影。

**示例 1:** 以下示例对世界进行 Bottomley 投影，中心位于(0，0)，无旋转。

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
    <script src=
"https://d3js.org/d3-geo-projection.v2.min.js">
    </script>
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

    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // Bottomley projection
        // Center(0,0) with 0 rotation
        var gfg = d3.geoBottomley()
            .scale(width / 1.5 / Math.PI)
            .rotate([0, 0])
            .center([0, 0])
            .translate([width / 2, height / 2])

        // Loading the json data
        d3.json(
            "https://raw.githubusercontent.com/"
            + "janasayantan/datageojson/master/"
            + "world.json",

            function (data) {
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

![](img/52f3b513e7ebc0b99176f7817dde8299.png)

y

**示例 2:** 以下示例在自定义中心和旋转后，对世界进行 Bottomley 投影。

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content=
        "width=device-width, initial-scale=1.0" />

    <script src="https://d3js.org/d3.v4.js">
    </script>
    <script src=
"https://d3js.org/d3-geo-projection.v2.min.js">
    </script>
</head>

<body>
    <div style="width:700px; height:900px;">
        <center>
            <h3 style="color:black">
            </h3>
        </center>
        <svg width="400" height="450">
        </svg>
    </div>

    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // Bottomley  projection
        // Center(0,20) and 45 degree 
        // rotation w.r.t Y axis
        var gfg = d3.geoBottomley()
            .scale(width / 1.5 / Math.PI)
            .rotate([-45, 0])
            .center([0, 20])
            .translate([width / 2, height / 2])

        // Loading the json data
        d3.json("https://raw.githubusercontent.com/"
            + "janasayantan/datageojson/master/world.json",
            function (data) {

                // Draw the map
                svg.append("g")
                    .selectAll("path")
                    .data(data.features)
                    .enter().append("path")
                    .attr("fill", "DarkOliveGreen")
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

![](img/2bd6eec2f04da6c8e4caf3d6fb36ef97.png)

相对于 Y 轴旋转 45 度并以(0，20)为中心的 Bottomley 投影