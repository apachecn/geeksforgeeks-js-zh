# 如何在 D3.js 中应用动画？

> 原文:[https://www . geesforgeks . org/how-apply-animation-in-D3-js/](https://www.geeksforgeeks.org/how-to-apply-animation-in-d3-js/)

[**D3.js**](https://www.geeksforgeeks.org/d3-js-data-driven-documents/) 是一个 Javascript 库，主要用于数据驱动的**文档**。D3 像在 HTML5 中一样使用了 SVG。使用 d3.js 可以完成制作图表、添加动画和可视化数据等许多事情。动画可以使用 d3.js 过渡功能来应用，该功能提供了许多功能，如延迟、缓解、淡入淡出、持续时间、缩放等。

**方法:**D3 中的动画可以借助 D3.js 提供的转场来完成，首先制作一个 div 元素，并在其中添加一些文字。然后使用 d3.select()函数选择这个元素。在此之后，使用 d3.js 中可用的转换函数在选定的 HTML 元素上应用动画。

**示例 1:** 本示例使用 d3.select()函数和 d3.transition()函数对 html 元素应用效果。

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" 
        content="width=device-width, 
                 initial-scale=1.0">
  <title>GeeksforGeeks</title>
</head>
<body>
  <div>
    <h3 style="color:green"> Geeks for Geeks</h3>
  </div>
  <script type = "text/javascript" 
          src = 
"https://d3js.org/d3.v4.min.js">
      </script>
  <script>
     d3.selectAll("h3").transition()
        .style(
"font-size", "50px").delay(1000).duration(1000)
  </script>
</body>
</html>
```

**输出:**

[![](img/29b7fd419d67724930812b5493cc427c.png)](https://media.geeksforgeeks.org/wp-content/uploads/20200826115832/chromecapture2.gif)

**例 2:**

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" 
        content="width=device-width, 
                 initial-scale=1.0">
  <title>Document</title>
</head>
<style>
  div{
    color:green;
    display: flex;
    margin: 0;
    font-size: xx-large;
    padding: 10px;
    width: 100%;
    justify-content: center;
    align-items: center;
    height: 100vh;
  }
</style>
<body>
  <div>
    <p> Geeks for Geeks</p>
  </div>
  <script type = "text/javascript" 
          src = "https://d3js.org/d3.v4.min.js">
  </script>
  <script>
     d3.selectAll("p").transition()
        .style(
"transform", "rotate(180deg)").delay(1000).duration(1000)
        .style("color", "black").duration(1000)
  </script>
</body>
</html>
```

**输出:**

[![](img/5be8f7b5609e416b60d565edc65debfe.png)](https://media.geeksforgeeks.org/wp-content/uploads/20200826115616/chromecapture1.gif)