# D3.js easePolyIn()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-easepolyin-function/](https://www.geeksforgeeks.org/d3-js-easepolyin-function/)

d3.js 中的 **d3.easePolyIn()** 函数用于多项式指数缓和对特定元素的过渡效果。这个指数宽松函数将时间提升到给定指数的幂。

**语法:**

```
d3.easePolyIn 

// Or 

d3.easePolyIn.exponent(t);

```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **t:** 是要升到指数幂的时间。

**返回值:**这个函数没有返回值。

**方法:** D3.js 转换函数将用于对特定元素应用不同的缓和效果。首先，创建一个 SVG 元素并将其附加到 HTML 页面的正文中，然后创建一个矩形或任何其他形状并将其附加到 SVG 中。设置矩形的一些属性，使其具有良好的颜色和大小，并应用 d3.transition 函数，然后使用 ease()函数，并使用 d3.easePolyIn 或 D3 . ease polyin . index(t)作为参数来使用 ease 函数。

**例 1:**

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">

    <script src = 
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <h1 style="color:green">GeeksforGeeks</h1>

    <svg width="500px" height="500px"></svg>
    <script>
        var svg = d3.select("svg")
            .attr("transform","translate(0,-50)");

        svg.append("rect")
            .attr("x", 10)
            .attr("y",50)
            .attr("width",150)
            .attr("height",50)
            .attr("fill", "green")
            .transition()

            // Use of d3.easePolyIn
            .ease(d3.easePolyIn)
            .attr("x", 100)
            .attr("y",100)
            .attr("width",150)
            .attr("height",200)
            .duration(2000);

    </script>
</body>

</html>
```

**输出:**

![](img/dfe9c9c58c5246966c1b0ffddb8e0a94.png)

**例 2:**

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">

    <script src = 
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <h1 style="color:green">GeeksforGeeks</h1>

    <svg width="500px" height="500px"></svg>
    <script>
        var svg = d3.select("svg")
            .attr("transform","translate(0,-50)");

        svg.append("rect")
            .attr("x", 10)
            .attr("y",50)
            .attr("width",150)
            .attr("height",50)
            .attr("fill", "green")
            .transition()

            // Use of d3.easePolyIn
            .ease(d3.easePolyIn.exponent(50))
            .attr("x", 100)
            .attr("y",100)
            .attr("width",150)
            .attr("height",200)
            .duration(2000);

    </script>
</body>

</html>
```

**输出:**

![](img/00e3707b5dc5f2dce9d7c0ae2e65e0bd.png)