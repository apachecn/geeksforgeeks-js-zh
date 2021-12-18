# D3.js axis.tickSize()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-axis-ticksize-function/](https://www.geeksforgeeks.org/d3-js-axis-ticksize-function/)

D3.js 中的 **d3.axis.tickSize()函数**用于将*内*和*外*的 tickSize 设置为指定值并返回坐标轴。如果未指定大小，则返回当前内部刻度大小，默认为 6。

**语法:**

```
axis.tickSize([size])
```

**参数:**该功能接受如上所述的单个参数，描述如下:

*   **大小:**此参数保存大小，以设置内部和外部刻度大小。

**返回值:**该函数返回坐标轴。

下面的程序说明了 D3.js 中的 **d3.axis.tickSize()** 功能:

**例 1:**

## 超文本标记语言

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        D3.js | D3.axis.tickSize() Function 
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

        var x_axis = d3.axisBottom() 
            .scale(xscale).tickSize(15); 

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

![](img/513403633786fb47a14412c9ee8397eb.png)

**例 2:**

## 超文本标记语言

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        D3.js | D3.axis.tickSize() Function 
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

        var y_axis = d3.axisRight() 
            .scale(yscale).tickSize(0);

        svg.append("g") 
            .attr("transform", "translate(100,20)") 
            .call(y_axis)  
    </script> 
</body> 
</html>
```

**输出:**

![](img/d8920786666c5c596da7e1689e28fca6.png)