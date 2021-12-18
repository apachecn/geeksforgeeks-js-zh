# D3 . js . brush . move()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-brush-move-function/](https://www.geeksforgeeks.org/d3-js-brush-move-function/)

**D3.js** 中的**笔刷. move()** 功能用于在指定的组中设置笔刷的活动选择。

**语法:**

```
brush.move(group, selection);
```

**参数:**该函数接受一个参数，如上所述，如下所述

*   **组:**该参数是指定的实现画笔的组。
*   **选择:**此参数为数字数组。

**返回值:**该函数返回定义该元素画笔选择的数组。

下面的程序说明了 **D3.js** 中的**笔刷. move()** 功能

**例 1:**

```
<!DOCTYPE html>  
<html>  

<head>  

    <script src=
        "https://d3js.org/d3.v5.min.js">
    </script> 
</head>  

<body>  
    <center>
        <h1 style="color:green;">GeeksForGeeks</h1>
        <h3>D3.js | brush.move() Function  </h3>

        <button>Click</button>
        <br>
        <br>
        <svg style="background-color: lightgreen;" 
             width="500" height="100">

             </svg> 

        <script>  

            // Selecting SVG element 
            const svg = d3.select("svg");

            const g = svg.append("g");

            // Creating a brush using the  
            // d3.brush function 
            g.call(d3.brush());

            // Use of brush.move() function
            d3.select("button").on("click", function() {
                g.call(d3.brush().move, [
                    [100, 0],
                    [400, 100]
                ])
            });     
        </script>  
    </center>
</body>  

</html>
```

**输出:**

<video class="wp-video-shortcode" id="video-472154-1" width="640" height="360" autoplay="" preload="metadata" controls=""><source type="video/webm" src="https://media.geeksforgeeks.org/wp-content/uploads/20200820131610/move1.webm?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/20200820131610/move1.webm](https://media.geeksforgeeks.org/wp-content/uploads/20200820131610/move1.webm)</video>

**例 2:**

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
      fill-opacity: 0.2;
    }

    circle.active {
      fill-opacity: 0.8;
      stroke: red;
      fill: green;
    }

    </style>
</head>  

<body>  
    <center>
        <h1 style="color:green;">GeeksForGeeks</h1>
        <h3>D3.js | brush.move() Function  </h3>

        <svg width="600" height="300"></svg>

        <script>  
            var data = d3.range(100).map(Math.random);

            var svg = d3.select("svg"),
                margin = {top: 50, right: 50,
                bottom: 50, left: 50},
                width = +svg.attr("width") - 
                margin.left - margin.right,
                height = +svg.attr("height") - 
                margin.top - margin.bottom,
                g = svg.append("g")
                    .attr("transform", "translate(" 
                    + margin.left + ", " + margin.top + ")"
                    );

            var x = d3.scaleLinear().range([0, width]),
                y = d3.randomNormal(height / 2, height / 8);

            var brush = d3.brushX()
                .extent([[0, 0], [width, height]])
                .on("start brush end", brushmoved);

            g.append("g")
                .attr("class", "axis axis--x")
                .attr("transform", "translate(0, 0)")
                .call(d3.axisTop(x));

            var circle = g.append("g")
                .attr("class", "circle")
              .selectAll("circle")
              .data(data)
              .enter().append("circle")
                .attr("transform", function (d) { 
                    return "translate(" 
                    + x(d) + ", " + y() + ")"; 
                })
                .attr("r", 10);

            var gBrush = g.append("g")
                .attr("class", "brush")
                .call(brush);

            gBrush.call(brush.move, [0.3, 0.5].map(x));

            var bs = "";
            function brushmoved() {
              var s = d3.event.selection;

              if (d3.event.type === "start"){
                bs = d3.event.selection;
              } else if (d3.event.type === "end"){
                if (bs[0] !== s[0] && bs[1] !== s[1]) {
                  console.log('moved both');
                } else if (bs[0] !== s[0]) {
                  console.log('moved left');
                } else {
                  console.log('moved right');
                }
              }

              if (s == null) {
                handle.attr("display", "none");
                circle.classed("active", false);
              } else {
                var sx = s.map(x.invert);
                circle.classed("active", function (d) {
                    return sx[0] <= d && d <= sx[1]; 
                });
                handle.attr("display", null)
                .attr("transform", function (d, i) {
                    return "translate("
                    + s[i] + ", " + height / 2 + ")"; 
                });
              }
            }

        </script>  
    </center>
</body>  

</html>  
```

**输出:**

<video class="wp-video-shortcode" id="video-472154-2" width="640" height="360" autoplay="" preload="metadata" controls=""><source type="video/webm" src="https://media.geeksforgeeks.org/wp-content/uploads/20200820131908/move2.webm?_=2">[https://media.geeksforgeeks.org/wp-content/uploads/20200820131908/move2.webm](https://media.geeksforgeeks.org/wp-content/uploads/20200820131908/move2.webm)</video>