# D3.js 刷()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-brush-function/](https://www.geeksforgeeks.org/d3-js-brush-function/)

D3 . js 中的 **d3.brush()函数** 用来新建一个 2d 画笔。画笔通常是由 SVG 元素创建的。

**语法:**

```
d3.brush();

```

**参数:**此功能不接受任何参数。

**返回值:**这个函数返回一个新创建的画笔。

**示例:**在本例中，我们将使用此方法在 SVG 元素上创建一个大小为 600×600 像素的画笔。

## 超文本标记语言

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        D3.js | d3.brush() Function 
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
        // Creating a brush using the 
        // d3.brush function
        .call( d3.brush()             
        // Initialise the brush area: start at 
        // 0,0 and finishes at given width,height
        .extent( [ [0,0], [600,600] ] )       
      )
    </script> 
</body> 

</html> 
```

**输出:**笔刷创建成功，可以用这个笔刷拖动创建矩形。

![](img/35376b593482fb0cb6da77ea17338fdb.png)
**参考:**[https://devdocs.io/d3~5/d3-brush#_brush](https://devdocs.io/d3~5/d3-brush#_brush)