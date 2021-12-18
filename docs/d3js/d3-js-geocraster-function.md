# D3 . js geograster()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-geocraster-function/](https://www.geeksforgeeks.org/d3-js-geocraster-function/)

**d3.js** 中的**geograster()**功能用于绘制给定 geojson 数据的 **Craster 抛物线投影**。卡斯特抛物线投影也被称为 Putniņš P4。

**语法**:

```
d3.geoCraster()

```

**参数:**此方法不接受任何参数。

**返回值:**此方法返回克拉斯特投影。

**示例 1** :以下示例绘制世界的 Craster 投影，中心在(0，0)，旋转 0 度。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script src="https://d3js.org/d3.v4.js">
    </script>
    <script src=
"https://d3js.org/d3-geo-projection.v2.min.js">
    </script>
</head>

<body>
    <div style="width:700px; height:500px;">
        <center>
            <h3 style="color:black"></h3>
        </center>
        <svg width="600" height="450">
        </svg>
    </div>

    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // Craster projection
        // Center at (0,0) with 0 degrees
        // rotation
        var gfg = d3.geoCraster()
            .scale(width / 1.8 / Math.PI)
            .rotate([0, 0])
            .center([0, 0])
            .translate([width / 2, height / 2]);

        // Loading the json data
        d3.json("https://raw.githubusercontent.com/" +
            "janasayantan/datageojson/master/" +
            "world.json",
            function (data) {

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
            });
    </script>
</body>

</html>
```

**输出:**

![](img/a576313a0ed7e2988dbbae80ca3ef42d.png)

**示例 2:** 以下示例绘制了以(0，20)为中心，相对于 y 轴旋转-45 度的世界的 Craster 投影。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script src="https://d3js.org/d3.v4.js">
    </script>
    <script src=
"https://d3js.org/d3-geo-projection.v2.min.js">
    </script>
</head>

<body>
    <div style="width:700px; height:600px;">
        <center>
            <h3 style="color:black"></h3>
        </center>
        <svg width="500" height="450">
        </svg>
    </div>

    <script>
        var svg = d3.select("svg"),
            width = +svg.attr("width"),
            height = +svg.attr("height");

        // Craster  projection
        // Center(0,20) and -45 degree
        // rotation w.r.t y-axis
        var gfg = d3.geoCraster()
            .scale(width / 1.8 / Math.PI)
            .rotate([-45, 0])
            .center([0, 20])
            .translate([width / 2, height / 2]);

        // Loading the json data
        d3.json("https://raw.githubusercontent.com/" +
            "janasayantan/datageojson/master/" +
            "world.json",
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
            });
    </script>
</body>

</html>
```

**输出:**

![](img/7f10a11d8553b7cb582fd207cf156be9.png)