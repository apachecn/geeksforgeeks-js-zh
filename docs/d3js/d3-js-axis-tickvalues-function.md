# D3.js 轴. tickValues()函数

> 原文:[https://www . geesforgeks . org/D3-js-axis-tick values-function/](https://www.geeksforgeeks.org/d3-js-axis-tickvalues-function/)

D3.js 中的 **d3.axis.tickValues()函数**用于生成特定值的刻度。该函数返回当前刻度值，默认为空。

**语法:**

```
axis.tickValues([values])
```

**参数:**该功能接受以下参数。

*   **值:**此参数用于刻度，而不是使用刻度的自动刻度生成器

**返回值:**该函数返回特定值的刻度。

**注意:**明确的刻度值优先于 **axis.tickArguments** 设置的刻度参数。

下面的程序说明了 D3.js 中的 **d3.axis.tickValues()** 函数:

**例 1:**

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        D3.js | D3.axis.tickValues() Function 
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

        var x_axis = d3.axisBottom(xscale)
        .tickValues([2, 4, 6, 7]); 

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

![](img/259deda8c2292d928265df6497352206.png)

**例 2:**

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        D3.js | D3.axis.tickValues() Function 
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

        var yscale = d3.scaleLinear() 
            .domain([0, 1]) 
            .range([height - 50, 0]); 

        var y_axis = d3.axisLeft()
        .scale(yscale).tickValues([ 0, 0.5, 1]); 

        svg.append("g") 
            .attr("transform", "translate(100, 20)") 
            .call(y_axis) 
    </script>
</body> 
</html>
```

**输出:**

![](img/752b02a9bfdbd265ef0969a5d4b58841.png)