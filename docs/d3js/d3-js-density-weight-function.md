# D3.js 密度.重量()函数

> 原文:[https://www . geesforgeks . org/D3-js-密度-重量-功能/](https://www.geeksforgeeks.org/d3-js-density-weight-function/)

**密度权重()**函数用于设置密度轮廓估计器函数的权重取值器。如果给定了权重，则该函数为点权重设置取值器，否则将取值器设置为默认值 1。

**语法:**

```
d3.contourDensity.x().y().weight([weight]);
```

**参数:**该函数取一个参数，如上所述，如下所述:

*   **权重:**取一个数字，用于设置点权重的取值器。

**返回值:**这个函数不返回任何东西。

下面给出了几个密度.重量()函数的例子。

**示例 1:**

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

        // append the svg object to the body.
        var svg = d3.select("body")
        .append("svg")
            .attr("width", 530)
            .attr("height", 480)
        .append("g")
            .attr("transform",
                "translate(" + 40 + ", " + -80 + ")");

        // read data
        d3.csv("./data.csv", function(data) {

        var y = d3.scaleLinear()
            .domain([2, 30])
            .range([ 300, 100 ]);

        var x = d3.scaleLinear()
            .domain([2, 22])
            .range([ 0, 200]);

        svg.append("g")
        .call(d3.axisLeft(y));

        svg.append("g")
            .attr("transform", "translate(0, " + 300 + ")")
            .call(d3.axisBottom(x));

        var density= d3.contourDensity()
            .y(function(d) { return y(d.y); })
            .bandwidth(15)
            // Use of weight function 
            .weight(0.007)
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

![](img/74b58712cf66924e5654b807a29f0d2e.png)

**示例 2:**

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

        // append the svg object to the body.
        var svg = d3.select("body")
        .append("svg")
            .attr("width", 530)
            .attr("height", 480)
        .append("g")
            .attr("transform",
                "translate(" + 40 + ", " + -80 + ")");

        // read data
        d3.csv("./data.csv", function(data) {

        var y = d3.scaleLinear()
            .domain([2, 30])
            .range([ 300, 100 ]);

        var x = d3.scaleLinear()
            .domain([2, 22])
            .range([ 0, 200]);

        svg.append("g")
        .call(d3.axisLeft(y));

        svg.append("g")
            .attr("transform", "translate(0, " + 300 + ")")
            .call(d3.axisBottom(x));

        var density= d3.contourDensity()
            .y(function(d) { return y(d.y); })
            .bandwidth(15)
            // Use of weight function 
            .weight(48888)
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

![](img/149bd6ce017becfc83088f77d63e061e.png)