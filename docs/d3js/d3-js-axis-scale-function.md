# D3.js 轴.刻度()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-axis-scale-function/](https://www.geeksforgeeks.org/d3-js-axis-scale-function/)

d3.axis.scale()函数在 D3.js 中用来设置刻度和返回坐标轴。如果此函数未提供指定的刻度，则返回当前刻度。

**语法:**

```
axis.scale([scale])

```

**参数:**该函数只接受一个参数，如上所述，如下所述:

*   **刻度:**该参数为可选参数，保存使用的刻度。

**返回值:**该函数返回坐标轴。

下面的程序说明了 D3.js 中的 d3.axis.scale()函数:

**例 1:**

## 超文本标记语言

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        D3.js | d3.axisBottom() Function 
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

        var x_axis = d3.axisBottom().scale(xscale); 

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

![](img/13b7cd0f01b5246873d092f997575b18.png)

**例 2:**

## 超文本标记语言

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        D3.js | d3.axisRight() Function 
    </title> 
    <script type="text/javascript"
        src="https://d3js.org/d3.v4.min.js"> 
    </script> 

    <style> 
        svg text { 
            fill: green; 
            font: 15px sans-serif; 
            text-anchor: start; 
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
            .domain([0, 10]) 
            .range([height - 50, 0]); 

        var y_axis = d3.axisRight().scale(yscale); 

        svg.append("g") 
            .attr("transform", "translate(100,20)") 
            .call(y_axis) 
    </script> 
</body> 
</html>
```

**输出:**

![](img/5a7709c6ddc547919052e2e696c1921c.png)