# D3.js geoGilbert()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-geogilbert-function/](https://www.geeksforgeeks.org/d3-js-geogilbert-function/)

JavaScript **D3.js** 库使用 HTML5、可缩放矢量图形和级联样式表为网页提供交互式数据可视化。 **d3.js** 中的 **geoGilbert()** 功能用于绘制 Gilbert 的两世界透视投影。

**语法:**

```
d3.geoGilbert([type])
```

**参数:**该方法接受一个参数，如上所述，如下所述。

*   **类型:**指定的投影类型，如果未指定，则为正投影。

**返回:**该方法根据给定的 JSON 数据创建吉尔伯特的两世界透视投影。

**示例 1:** 以下示例对世界进行吉尔伯特投影，中心在(0，0)且无旋转。

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, 
                initial-scale=1.0" />
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

        // Gilbert  projection
        // Center(0, 0) with 0 rotation
        var gfg = d3.geoGilbert()
            .scale(width / 1.5 / Math.PI)
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

![](img/39a269727279d93e9546041acab07df3.png)

**示例 2:** 以下示例在改变中心和旋转后对世界进行吉尔伯特投影。

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, 
                initial-scale=1.0" />
    <script src="https://d3js.org/d3.v4.js"></script>
    <script src=
"https://d3js.org/d3-geo-projection.v2.min.js">
    </script>
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

        // Fahey  projection
        // Center(0, 10) and 45 degree 
        // rotation w.r.t Y axis
        var gfg = d3.geoGilbert()
            .scale(width / 1.5 / Math.PI)
            .rotate([-45, 0])
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
![](img/8a6c6261a0a2832e3afcbbf7c96e9efa.png)