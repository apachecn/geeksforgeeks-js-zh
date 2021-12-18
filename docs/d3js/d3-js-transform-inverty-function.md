# D3.js transform.invertY()函数

> 原文:[https://www . geesforgeks . org/D3-js-transform-inverty-function/](https://www.geeksforgeeks.org/d3-js-transform-inverty-function/)

**D3.js** 库中的 **transform.invertY()** 函数用于获取指定 y 坐标的逆变换，(y–t<sub>y</sub>)/k。

**语法:**

```
transform.invertY( y )
```

**参数:**该功能接受如下参数，如上所述，描述如下

*   **y:** 此参数为 y 坐标。

**返回值:**该函数返回变换后的缩放行为。

下面的程序说明了 **D3.js** 库中的 **transform.invertY()** 函数。

**例 1:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8">

    <script src="https://d3js.org/d3.v4.min.js">
    </script>

    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/d3/5.7.0/d3.min.js">
    </script>
</head>

<body>
    <center>
        <h1 style="color: green;">
            Geeksforgeeks
        </h1>

        <h3>D3.js | transform.invertY() Function</h3>

        <svg width="300" height="300">
            <g>
                <image xlink: href=
"https://media.geeksforgeeks.org/wp-content/cdn-uploads/20190710102234/download3.png"
                x="150" y="150" width="50" height="50">
                </image>
            </g>
        </svg>

        <script>
            var zoom = d3.zoom()
                .on("zoom", zoomed)
                .constrain(constr);

            var svg = d3.select("svg").call(zoom),
                g = svg.select("g"),
                image = g.select("image"),
                width = +svg.attr("width"),
                height = +svg.attr("height"),
                x0 = +image.attr("x"),
                y0 = +image.attr("y"),
                x1 = +image.attr("width") + x0,
                y1 = +image.attr("height") + y0;

            zoom.scaleExtent([1, Math.min(width /
                (x1 - x0), height / (y1 - y0))]);

            function zoomed() {
                var trans = d3.event.transform;
                if (trans.invertX(0) > x0)
                    trans.x = -x0 * trans.k;
                else if (trans.invertX(width) < x1)
                    trans.x = width - x1 * trans.k;
                if (trans.invertY(0) > y0)
                    trans.y = -y0 * trans.k;
                else if (trans.invertY(height) < y1)
                    trans.y = height - y1 * trans.k;
                g.attr("transform", trans);
            }

            function constr(transform, extent, 
                            translateExtent) {
                var dx0 = transform.invertX(
                        extent[0][0]) - translateExtent[0][0],

                    dx1 = transform.invertX(
                        extent[1][0]) - translateExtent[1][0],

                    dy0 = transform.invertY(
                        extent[0][1]) - translateExtent[0][1],

                    dy1 = transform.invertY(
                        extent[1][1]) - translateExtent[1][1];

                return transform.translate(
                    dx1 > dx0 ? (dx0 + dx1) / 2 : 
                        Math.min(0, dx0) || Math.max(0, dx1),

                    dy1 > dy0 ? (dy0 + dy1) / 2 : 
                        Math.min(0, dy0) || Math.max(0, dy1)
                );
            }
        </script>
    </center>
</body>

</html>
```

**输出:**

![](img/010ab8fdcf26a08d357c641e5e2fa167.png)

**例 2:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8">

    <script src=
        "https://d3js.org/d3.v4.min.js">
    </script>

    <style>
        circle {
            opacity: 0.7;
        }
    </style>
</head>

<body>
    <center>
        <h1 style="color: green;">
            Geeksforgeeks
        </h1>

        <h3>D3.js | zoom.invertY() Function</h3>

        <svg></svg>

        <script>
            var radius = 15;
            var svg = d3.select('svg');
            var dimension = document.body
                .getBoundingClientRect();

            var data = d3.range(0, 50).map(function () {
                return {
                    x: getRandom(radius, 400 - radius),
                    y: getRandom(radius, 200 - radius)
                }
            });

            var zoom = d3.zoom()
                .constrain(mydata)
                .on('zoom', function () {
                    canvas.attr('transform', 
                            d3.event.transform);
                })

            var canvas = svg.attr('width', 400)
                .attr('height', 200)
                .call(zoom)
                .insert('g', ':first-child');

            canvas.selectAll('circle')
                .data(data)
                .enter()
                .append('circle')
                .attr('r', radius)
                .attr('cx', function (d) {
                    return d.x;
                })
                .attr('cy', function (d) {
                    return d.y;
                })
                .style('fill', function () {
                    return d3.schemeCategory10
                            [getRandom(0, 9)]
                });

            function getRandom(min, max) {
                min = Math.ceil(min);
                max = Math.floor(max);
                return Math.floor(Math.random() 
                        * (max - min + 1)) + min;
            }

            function mydata(transform, extent, 
                            translateExtent) {
                var dx0 = transform.invertX(
                        extent[0][0]) - translateExtent[0][0],

                    dx1 = transform.invertX(
                        extent[1][0]) - translateExtent[1][0],

                    dy0 = transform.invertY(
                        extent[0][1]) - translateExtent[0][1],

                    dy1 = transform.invertY(
                        extent[1][1]) - translateExtent[1][1];

                return transform.translate(
                    dx1 > dx0 ? (dx0 + dx1) / 2 : 
                        Math.min(0, dx0) || Math.max(0, dx1),

                    dy1 > dy0 ? (dy0 + dy1) / 2 : 
                        Math.min(0, dy0) || Math.max(0, dy1)
                );
            }
        </script>
    </center>
</body>

</html>
```

**输出:**

![](img/f8293e97e8b7b97fb820a0600c0f4c69.png)