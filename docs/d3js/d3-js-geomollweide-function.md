# D3.js geoMollweide()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-geomollweide-function/](https://www.geeksforgeeks.org/d3-js-geomollweide-function/)

D3.js 是一个 JavaScript 库，用于在 web 浏览器中产生动态的、交互式的数据可视化。它利用了可伸缩矢量图形、HTML5 和级联样式表标准。d3.js 中的 geoMercator()函数用于绘制等面积的伪圆柱形 Mollweide 投影。

**语法:**

```
d3.geoMollweide()
```

**参数:**此方法不接受任何参数。

**返回:**该方法根据给定的 json 数据创建莫勒维德投影。

**示例#1:** 以下示例绘制了以(0，0)为中心，0°旋转的世界的 Mollweide 投影。

```
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta
            name="viewport"
            content="width=device-width, 
                initial-scale=1.0"
        />
    </head>

    <body>
        <div style="width: 700px; height: 500px;">
            <center>
                <h3 style="color: black;"></h3>
            </center>

            <svg width="600" height="450"></svg>
        </div>
        <script src="https://d3js.org/d3.v4.js"></script>
        <script src=
                "https://d3js.org/d3-geo-projection.v2.min.js">
      </script>
        <script>
            var svg = d3.select("svg"),
                width = +svg.attr("width"),
                height = +svg.attr("height");

            // Mollweide projection
            // Center(0, 0) with 0 rotation
            var gfg = d3
                .geoMollweide()
                .scale(width / 1.5 / Math.PI)
                .rotate([0, 0])
                .center([0, 0])
                .translate([width / 2, height / 2]);

            // Loading the json data
            // Used json file stored at
/*https://raw.githubusercontent.com/janasayantan
            /datageojson/master/world.json*/
            d3.json(
"https://raw.githubusercontent.com/janasayantan/datageojson/master/world.json",
              function (data) {
                // Drawing the map
                svg.append("g").selectAll(
                  "path").data(data.features).enter().append(
                  "path").attr("fill", "SaddleBrown").attr(
                  "d", d3.geoPath().projection(gfg)).style(
                  "stroke", "#ffff");
            });
        </script>
    </body>
</html>
```

**输出:**

![](img/b8385034458be858c4c0dbda53d8c1d2.png)

世界的莫勒维德投影，无旋转，以(0，0)为中心

**示例#2:** 以下示例绘制了改变中心和旋转后的 Mollweide 世界投影。

```
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta
            name="viewport"
            content="width=device-width, 
                initial-scale=1.0"
        />
    </head>

    <body>
        <div style="width: 700px; height: 600px;">
            <center>
                <h3 style="color: black;"></h3>
            </center>

            <svg width="500" height="450"></svg>
        </div>
        <script src="https://d3js.org/d3.v4.js"></script>
        <script src=
                "https://d3js.org/d3-geo-projection.v2.min.js">
      </script>
        <script>
            var svg = d3.select("svg"),
                width = +svg.attr("width"),
                height = +svg.attr("height");

            // Mollweide  projection
     // Center(0, 20) and 90 degree rotation w.r.t Y axis
            var gfg = d3
                .geoMollweide()
                .scale(width / 1.7 / Math.PI)
                .rotate([90, 0])
                .center([0, 20])
                .translate([width / 2, height / 2]);

            // Loading the json data
            // Used json file stored at
 /*https://raw.githubusercontent.com/janasayantan
            /datageojson/master/world.json*/
            d3.json(
"https://raw.githubusercontent.com/janasayantan/datageojson/master/world.json",
              function (data) {
                // Draw the map
                svg.append("g").selectAll(
                  "path").data(data.features).enter().append(
                  "path").attr("fill", "Sienna").attr(
                  "d", d3.geoPath().projection(gfg)).style(
                  "stroke", "#ffff");
            });
        </script>
    </body>
</html>
```

**输出:**

![](img/26e66cdf63049ce36b2b54b449400152.png)

相对于 Y 轴旋转 90 度并以(0，20)为中心的莫勒维德投影