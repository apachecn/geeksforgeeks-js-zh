# D3.js ribbon.endAngle()功能

> 原文:[https://www . geesforgeks . org/D3-js-ribbon-endangle-function/](https://www.geeksforgeeks.org/d3-js-ribbon-endangle-function/)

**D3.js** 中的 **ribbon.endAngle()** 函数用于将结束角度访问器设置为指定的函数，并返回该 ribbon 生成器。

**语法:**

```
ribbon.endAngle([angle]);
```

**参数:**该函数接受一个参数，如上所述，如下所述

*   **角度:**此参数是设置结束角度取值器的弧度值。

**返回值:**该函数返回色带生成器。

以下程序说明了 **D3.js** 中的 **ribbon.endAngle()** 功能

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

        <h3>D3.js | ribbon.endAngle() Function</h3>
        <div id="GFG"></div>

        <script>
            // Create the svg area
            var svg = d3.select("#GFG")
                .append("svg")
                .attr("width", 300)
                .attr("height", 300)
                .append("g")
                .attr("transform", "translate(150, 150)")

            // Create input data
            var data = [[18, 6, 1, 4, 5, 1],
                [ 0, 80, 0, 2, 34, 53],
                [75, 16, 8, 0, 0, 3],
                [3, 9, 9, 6, 35, 4],
                [1, 0, 7, 3, 5, 1]];

            // Give this matrix to d3.chord()
            var chords = d3.chord()
                .padAngle(0.2) 
                .sortSubgroups(d3.ascending)
                .sortChords(d3.ascending)
                (data)

            var ribboon = d3.ribbon().radius(140)  
                .startAngle(2.2)

                // Use of ribbon.endAngle() function
                .endAngle(4.5);

            svg.datum(chords)
                .append("g")
                .selectAll("path")
                .data(function (d) { return d; })
                .enter()
                .append("path")
                .attr("d", ribboon)
                .style("fill", "#57beff")
                .style("stroke", "black");
        </script> 
    </center>
</body> 

</html>
```

**输出:**

![](img/05e2d30bb7cfa16902fd3f9e20709c4e.png)

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

            var rib = d3.ribbon().radius(150)
                .startAngle(1)
                // Use of ribbon.endAngle() function
                .endAngle(5)

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

![](img/979fac99e6e283e5a4182c4eb62cc2f8.png)