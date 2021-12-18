# D3.js ribbon.radius()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-ribbon-radius-function/](https://www.geeksforgeeks.org/d3-js-ribbon-radius-function/)

**D3.js** 中的 **ribbon.radius()** 函数用于将 radius 访问器设置为指定的函数，并返回该 ribbon 生成器。

**语法:**

```
ribbon.radius([radius]);
```

**参数:**该功能接受如上所述的单个参数，描述如下

*   **半径:**该参数是设置半径取值器的功能。

**返回值:**该函数返回色带生成器。

以下程序说明了 **D3.js** 中的 **ribbon.radius()** 功能

**例 1:**

```
<!DOCTYPE html> 
<html> 

<head> 
    <meta charset="utf-8">
    <script src="https://d3js.org/d3.v4.js"></script>
</head> 

<body>
    <center> 
        <h1 style="color:green;">GeeksForGeeks</h1>

        <h3>D3.js | ribbon.radius() Function</h3>
        <div id="GFG"></div>

        <script>
            // Create the svg area
            var svg = d3.select("#GFG")
                .append("svg")
                .attr("width", 340)
                .attr("height", 340)
                .append("g")
                .attr("transform", "translate(170, 170)")

            // Create input data
            var data = [[148, 60, 71, 34, 5, 1],
                [ 10, 80, 80, 12, 34, 53],
                [175, 16, 68, 0, 0, 3],
                [13, 9, 69, 76, 35, 4],
                [51, 60, 71, 34, 5, 1]];

            // Give this matrix to d3.chord()
            var chords = d3.chord()(data)

            var ribboon = d3.ribbon()
                // Use of ribbon.radius() function
                .radius(170);

            svg.datum(chords)
                .append("g")
                .selectAll("path")
                .data(function (d) { return d; })
                .enter()
                .append("path")
                .attr("d", ribboon)
                .style("fill", "#ffb357")
                .style("stroke", "black");
        </script> 
    </center>
</body> 

</html>
```

**输出:**

![](img/702efe78bb2958f8e9eb7df957c8a65f.png)

**例 2:**

```
<!DOCTYPE html> 
<html>

<head> 
    <meta charset="utf-8">

    <script src= "https://d3js.org/d3-color.v1.min.js">
    </script>  
    <script src= 
        "https://d3js.org/d3-interpolate.v1.min.js">
    </script>  
    <script src= 
        "https://d3js.org/d3-scale-chromatic.v1.min.js">
    </script>
</head> 

<body> 
    <center> 
        <h1 style="color:green;">GeeksForGeeks</h1>

        <h3>D3.js | ribbon.radius() Function</h3>
        <div id="GFG"></div>

        <script>
            // Create the svg area
            var svg = d3.select("#GFG")
                .append("svg")
                .attr("width", 320)
                .attr("height", 320)
                .append("g")
                .attr("transform", "translate(160, 160)")

            // Create input data
            var data = [[0,  58, 71, 89, 16, 28, 68, 0],
                [0, 19, 51, 0, 20, 60, 61, 71],
                [80, 10, 16, 145, 0, 80, 45, 0],
                [0, 10, 13, 9, 90,  94, 0, 0],
                [0, 0, 0, 0, 0, 0, 0, 0]];

            // 4 groups, so create a vector of 4 colors
            var colors = [d3.schemeSet1[7], d3.schemeSet1[6],
                d3.schemeSet1[5], d3.schemeSet1[4],
                d3.schemeSet1[3], d3.schemeSet1[2],
                d3.schemeSet1[1], d3.schemeSet1[0]];

            // Give this matrix to d3.chord()
            var chords = d3.chord()(data)

            var rib = d3.ribbon()
                // Use of ribbon.radius() function
                .radius(150);

            svg.datum(chords)
                .append("g")
                .selectAll("path")
                .data(function (d) { return d; })
                .enter()
                .append("path")
                .attr("d", rib)
                .style("fill", function (d) { 
                    return (colors[d.source.index])
                })
                .style("stroke", "black");
        </script> 
    </center>
</body>

</html>
```

**输出:**

![](img/114b0c83dd2d08bf6014a319d7f70cd5.png)