# D3.js 密度. x()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-density-x-function/](https://www.geeksforgeeks.org/d3-js-density-x-function/)

**density.x()** 功能用于设置 x 坐标访问器。如果未指定 x，则此函数返回当前的 x 坐标访问器。

**语法:**

```
d3.contourDensity.x([x]);
```

**参数:**该函数取一个参数，如上所述，如下所述:

*   **x:** 是 x 坐标访问器的值。

**返回值:**该函数返回一个数字。

下面给出了几个密度函数的例子。

**例 1:**

```
<!DOCTYPE html> 
<html lang="en"> 

<head> 
    <meta charset="UTF-8"> 
    <meta name="viewport" content=" 
        width=device-width, initial-scale=1.0"> 

    <script type="text/javascript"
        src="https://d3js.org/d3.v4.min.js"> 
    </script> 
    <script src=
"https://d3js.org/d3-contour.v1.min.js">
     </script>
</head> 

<body> 
    <h1 style="color:green">GeeksforGeeks</h1>

    <script> 

        // Append the svg object to the body.
        var svg = d3.select("body")
        .append("svg")
            .attr("width", 530)
            .attr("height", 480)
        .append("g")
            .attr("transform",
                "translate(" + 40 + ", " + 0 + ")");

        // Read data
        d3.csv("./data.csv", function(data) {

        var y = d3.scaleLinear()
            .domain([5, 30])
            .range([ 450, 10 ]);

        var x = d3.scaleLinear()
            .domain([5, 22])
            .range([ 0, 460]);

        svg.append("g")
        .call(d3.axisLeft(y));

        svg.append("g")
            .attr("transform", 
                  "translate(0, " + 450 + ")")
            .call(d3.axisBottom(x));

        var density= d3.contourDensity()
            .y(function(d) { return y(d.y); })
            .bandwidth(25)

            // Use of  density.x() function
            .x(function(d) { return x(d.x); })(data)

        svg.selectAll("path")
            .data(density)
            .enter()
            .append("path")
            .attr("d", d3.geoPath())
            .attr("fill", "none")
            .attr("stroke", "green")
        });

        // Data for csv file
        // x, y, group
        // 9.45, 14.14, H
        // 9.1, 14.14, H
        // 9.9, 9.9, H
        // 9.6, 14.5, H
        // 9.1, 9.7, H
        // 14.7, 9.5, H
        // 7.9, 9.6, H
        // 14.7, 9.7, H
        // 9.45, 14.14, H
        // 12.1, 9.14, H
        // 7.5, 9, H
        // 14.5, 14.5, H
        // 9.45, 9.7, H
        // 14.45, 9.6, H
        // 9.5, 7.6, H
        // 9, 9.45, H
        // 14.7, 12, H
        // 9.7, 9.7, H
        // 9.6, 9, H
        // 12, 9, H
        // 9.45, 14.5, H
        // 9.9, 14.6, H
        // 12.7, 9.9, H
        // 9, 12.14, H
        // 9, 14.9, H
        // 9.5, 9.7, H
        // 9.7, 14.7, H
        // 9.9, 14.5, H
        // 14, 14.5, H
        // 7.9, 9, H
        // 9.9, 9.45, H
        // 9, 14.14, H
        // 14.7, 9.7, H
        // 14.5, 9.9, H
    </script> 
</body> 

</html> 
```

**输出:**

![](img/1268de87a4eea1f340c4460221cc6c67.png)

**例 2:**

```
<!DOCTYPE html> 
<html lang="en"> 

<head> 
    <meta charset="UTF-8"> 
    <meta name="viewport" content=" 
        width=device-width, initial-scale=1.0"> 

    <script type="text/javascript"
        src="https://d3js.org/d3.v4.min.js"> 
    </script> 
    <script src=
"https://d3js.org/d3-contour.v1.min.js">
      </script>
</head> 

<body> 
    <h1 style="color:green">GeeksforGeeks</h1>

    <script> 

        // Append the svg object to the body.
        var svg = d3.select("body")
        .append("svg")
            .attr("width", 530)
            .attr("height", 480)
        .append("g")
            .attr("transform",
                "translate(" + 40 + ", " + 0 + ")");

        // Read data
        d3.csv("./data.csv", function(data) {

        var y = d3.scaleLinear()
            .domain([5, 30])
            .range([ 450, 10 ]);

        var x = d3.scaleLinear()
            .domain([5, 22])
            .range([ 0, 460]);

        svg.append("g")
        .call(d3.axisLeft(y));

        svg.append("g")
            .attr("transform", "translate(0, " + 450 + ")")
            .call(d3.axisBottom(x));

        var density= d3.contourDensity()
            .y(function(d) { return y(d.y); })
            .bandwidth(25)

            // Use of  density.x() function
            .x(function(d) { return x(d.x); })(data)

        svg.selectAll("path")
            .data(density)
            .enter()
            .append("path")
            .attr("d", d3.geoPath())
            .attr("fill", "green")
        });

        // Data for csv file
        // x, y, group
        // 9.45, 14.14, H
        // 9.1, 14.14, H
        // 9.9, 9.9, H
        // 9.6, 14.5, H
        // 9.1, 9.7, H
        // 14.7, 9.5, H
        // 7.9, 9.6, H
        // 14.7, 9.7, H
        // 9.45, 14.14, H
        // 12.1, 9.14, H
        // 7.5, 9, H
        // 14.5, 14.5, H
        // 9.45, 9.7, H
        // 14.45, 9.6, H
        // 9.5, 7.6, H
        // 9, 9.45, H
        // 14.7, 12, H
        // 9.7, 9.7, H
        // 9.6, 9, H
        // 12, 9, H
        // 9.45, 14.5, H
        // 9.9, 14.6, H
        // 12.7, 9.9, H
        // 9, 12.14, H
        // 9, 14.9, H
        // 9.5, 9.7, H
        // 9.7, 14.7, H
        // 9.9, 14.5, H
        // 14, 14.5, H
        // 7.9, 9, H
        // 9.9, 9.45, H
        // 9, 14.14, H
        // 14.7, 9.7, H
        // 14.5, 9.9, H
    </script> 
</body> 

</html> 
```

**输出:**

![](img/6543062da754ffd7f47a6ca90ffa84e6.png)