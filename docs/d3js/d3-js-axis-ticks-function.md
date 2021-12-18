# D3.js 轴. ticks()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-axis-ticks-function/](https://www.geeksforgeeks.org/d3-js-axis-ticks-function/)

D3.js 中的 **d3.axis.tickss()函数**用于控制轴显示哪些 tick。该函数返回轴生成器

**语法:**

```
axis.ticks(arguments…)
axis.ticks([count[, specifier]])
axis.ticks([interval[, specifier]])
```

**参数:**该功能接受以下参数。

*   **计数/间隔:**此参数用于显示刻度数。
*   **说明符:**此参数是可选的格式说明符，用于自定义刻度值的格式。

**返回值:**该函数返回轴生成器。

下面的程序说明了 D3.js 中的 **d3.axis.ticks()** 函数:

**例 1:**

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        D3.js | D3.axis.ticks() Function 
    </title> 
    <script type="text/javascript"
        src="https://d3js.org/d3.v4.min.js"> 
    </script> 

    <style> 
        svg text { 
            fill: green; 
            font: 15px sans-serif; 
            text-anchor: center; 
        } 
    </style> 
</head> 

<body> 
    <script> 
        var width = 400, height = 400; 
        var svg = d3.select("body") 
            .append("svg") 
            .attr("width", width) 
            .attr("height", height); 

        var xscale = d3.scaleLinear() 
            .domain([0, 10]) 
            .range([0, width - 60]); 

        var x_axis = d3.axisBottom().scale(xscale).ticks(5); 

        var xAxisTranslate = height / 2; 

        svg.append("g") 
            .attr("transform", "translate(50, " 
            + xAxisTranslate + ")") 
            .call(x_axis) 
    </script> 
</body> 
</html>
```

**输出:**

![](img/c54365612783846980301c6e9a1dcf28.png)

**例 2:**

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        D3.js | d3.axis.ticks() Function 
    </title> 
    <script type="text/javascript"
        src="https://d3js.org/d3.v4.min.js"> 
    </script> 

    <style> 
        svg text { 
            fill: green; 
            font: 15px sans-serif; 
            text-anchor: end; 
        } 
    </style> 
</head> 

<body> 
    <script> 
        var width = 400, height = 400; 
        var svg = d3.select("body") 
            .append("svg") 
            .attr("width", width) 
            .attr("height", height); 

        var yscale = d3.scaleLinear() 
            .domain([0, 1]) 
            .range([height - 50, 0]); 

        var y_axis = d3.axisLeft().scale(yscale).ticks(3, "$.2f"); 

        svg.append("g") 
            .attr("transform", "translate(100, 20)") 
            .call(y_axis) 
    </script> 
</body> 
</html>
```

**输出:**

![](img/05ca54d9bc4c48b9ccc368f59889f9e7.png)