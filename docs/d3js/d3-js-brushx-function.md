# D3 . js brusxx()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-brushx-function/](https://www.geeksforgeeks.org/d3-js-brushx-function/)

D3 . js 中的 **d3.brushX()函数** 用于 c 沿着 *x* 维度创建一个新的一维笔刷。

**语法:**

```
d3.brushX();

```

**参数:**此功能不接受任何参数。

**返回值:**该函数沿 x 轴返回新创建的一维画笔

**示例:**在本例中，我们将使用此方法在一个 SVG 元素上创建一个一维笔刷以及大小为 600×600 像素的 x 轴笔刷。

## 超文本标记语言

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        D3.js | d3.brushX() Function 
    </title> 

    <script src = 
        "https://d3js.org/d3.v4.min.js"> 
    </script> 
</head> 

<body> 
    <svg width=600 height=600 id="brush"></svg>
    <script> 

        // Selecting SVG element
        d3.select("#brush")
        // Creating a brush along x-axis 
        // using the d3.brush function
        .call( d3.brushX()             
        // Initialise the brush area: start at 
        // 0,0 and finishes at given width,height
        .extent( [ [0,0], [600,600] ] )       
      )
    </script> 
</body> 

</html>
```

**输出:**

![](img/7a6b16b7ddec2451a65e5e3912d9a3ec.png)

**参考:**T2】https://devdocs.io/d3~5/d3-brush#brushX