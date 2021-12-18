# D3 . js easemilionout()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-easepolyinout-function/](https://www.geeksforgeeks.org/d3-js-easepolyinout-function/)

d3.js 中的**D3 .Easer 聚利 nOut()** 函数被用来作为 D3 .Easer 聚利函数的别名。此功能用于为特定元素提供对称的缓和过渡效果。这个函数返回一个多项式函数。

**方法:** D3.js 转换函数将用于对特定元素应用不同的缓和效果。首先，创建一个 SVG 元素并将其附加到 HTML 页面的正文中，然后创建一个圆形或矩形或任何其他形状并将其附加到 SVG 中。设置特定形状的一些属性，使其具有良好的颜色和大小，并应用 d3.transition 函数，然后使用 ease()函数，并将 d3.easePolyInOut 作为该函数的参数。

**语法:**

```
svg.append().attr().ease(d3.easePolyInOut).attr();
```

**参数:**此功能不接受任何参数。

**返回值:**这个方法返回一个函数。

下面是上面给出的函数的几个例子。

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
</head> 
<body> 
    <h1 style="color:green">GeeksforGeeks</h1> 
    <svg width="600px" height="600px"></svg> 

    <script> 
        var svg = d3.select("svg")  
        svg.append("rect") 
        .attr("x", 50) 
        .attr("width", 10)
        .attr("height", 10)
        .attr("fill", "green") 
        .transition()
        .ease(d3.easePolyInOut) 
        .attr("width", 100)
        .attr("height", 100)
        .attr("fill", "red")
        .duration(1000); 
    </script> 
</body> 
</html> 
```

**输出:**

![](img/bac10060642c802e5b4dfdb77b8f740b.png)

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
</head> 
<body> 
    <h1 style="color:green">GeeksforGeeks</h1> 
    <svg width="600px" height="600px"></svg> 

    <script> 
       var svg = d3.select("svg")  
       svg.append("circle") 
       .attr("r", 0) 
       .attr("cx", 100)
       .attr("cy", 50)
       .attr("fill", "green") 
       .transition()
       .delay(8000)
       .ease(d3.easePolyInOut) 
       .attr("r", 50)
       .duration(1000); 
    </script> 
</body> 
</html> 
```

**输出:**

![](img/79baf137eab34727f0c086b681a72aae.png)