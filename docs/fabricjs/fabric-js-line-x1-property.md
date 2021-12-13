# 布艺. js 线 x1 属性

> 原文:[https://www.geeksforgeeks.org/fabric-js-line-x1-property/](https://www.geeksforgeeks.org/fabric-js-line-x1-property/)

在本文中，我们将使用 **x1** 属性来获取 **FabricJS** 中画布线的 x1。帆布线是指线是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义线条。

为了实现这一点，我们将使用一个名为 **FabricJS** 的 JavaScript 库。导入库之后，我们将在主体标签中创建一个画布块，它将包含行。之后，我们将初始化 **FabricJS** 和提供的画布和线条实例，使用 **x1** 属性获取画布线条的 x1，并在画布上渲染线条，如下所示。

**语法:**

```html
var x = line.x1
```

**参数:**该属性接受如上所述的单个参数，如下所述:

*   **x1** **:** 指定画布线的 x1。包含数值。

**示例 1:**

## 超文本标记语言

```html
<!DOCTYPE html>
<html>

<head>

   <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
   </script>
</head>

<body>
   <h1>fabric.js | line x1  property</h1>
   <canvas id="canvas" width="600" height="200"
      style="border:1px solid #000000;">
   </canvas>

   <script>

      var canvas = new fabric.Canvas("canvas");

      var line = new fabric.Line([150, 10, 220, 150], {
         stroke: 'green',
      });

      canvas.add(line);
      alert("x1 point of the line is :"+line.x1)
   </script>
</body>

</html>
```

**输出:**

![](img/5d4d60215938f8aefbe9545bc1096cdf.png)