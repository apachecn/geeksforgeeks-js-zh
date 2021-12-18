# D3.js axis.tickSizeOuter()函数

> 原文:[https://www . geesforgeks . org/D3-js-axis-ticksizeouter-function/](https://www.geeksforgeeks.org/d3-js-axis-ticksizeouter-function/)

D3.js 中的 **d3.axis.tickSizeOuter()函数**用于将外刻度尺寸设置为指定值并返回坐标轴。外部刻度尺寸控制从轴的原始位置偏移的域路径的正方形末端的长度。

**语法:**

```
axis.tickSizeOuter([size])

```

**参数:**该功能接受如上所述的单个参数，描述如下:

*   **大小:**此参数为大小，用于设置内、外刻度大小。

**返回值:**该函数返回坐标轴。

下面的程序说明了 D3.js 中的 **d3.axis.tickSizeOuter()** 函数:

**例 1:**

## 超文本标记语言

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        D3.js | D3.axis.tickSizeOuter() Function 
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
            .scale(xscale).tickSizeOuter([40]).tickSizeInner([0]);

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

![](img/0115957c7505755ec8cc2ed32e396219.png)

**例 2:**

## 超文本标记语言

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        D3.js | D3.axis.tickSizeOuter() Function 
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

        var y_axis = d3.axisRight() 
            .scale(yscale).tickSizeOuter([20]);

        svg.append("g") 
            .attr("transform", "translate(100,20)") 
            .call(y_axis)  
    </script> 
</body> 
</html>
```

**输出:**

![](img/51a7b45a8d090a38a93ac22e6a6a5f20.png)