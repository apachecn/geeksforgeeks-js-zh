# Fabric.js 多边形动画属性

> 原文:[https://www . geesforgeks . org/fabric-js-polygon-flipy-property/](https://www.geeksforgeeks.org/fabric-js-polygon-flipy-property/)

在本文中，我们将看到如何在 FabricJS 中设置画布多边形的垂直翻转。画布多边形是指多边形是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义多边形。

**方法:**为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。导入库之后，我们将在主体标签中创建一个包含多边形的画布块。之后，我们将初始化由 FabricJS 提供的 Canvas 和多边形的实例，并使用 flipY 属性垂直翻转多边形，并在多边形上渲染 Canvas，如下例所示。

**语法:**

```
fabric.Polygon([
          { x: pixel, y: pixel },
          { x: pixel, y: pixel },
          { x: pixel, y: pixel},
          { x: pixel, y: pixel},
          { x: pixel, y: pixel }],
          {
              flipY: boolean
          });

```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **翻转:**指定画布对象的垂直翻转。

**注意:**尺寸像素是必须创建的多边形。

下面的例子说明了织物。JavaScript 中的 JS 多边形**动画**属性:

**示例:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>

    <!-- Loading the FabricJS library -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <div style="text-align: center;width: 600px;">
        <h1 style="color: green;">
            GeeksforGeeks
        </h1>
        <b>
            Fabric.js | Polygon flipY Property
        </b>
    </div>
    <canvas id="canvas" width="600" height="200" 
        style="border:1px solid #000000;">
    </canvas>

    <script>
        // Initiate a Canvas instance 
        var canvas = new fabric.Canvas("canvas");

        // Initiate a polygon instance 
        var polygon = new fabric.Polygon([
            { x: 295, y: 10 },
            { x: 235, y: 198 },
            { x: 385, y: 78 },
            { x: 205, y: 78 },
            { x: 355, y: 198 }], {
            flipY: true
        });

        // Render the polygon in canvas 
        canvas.add(polygon); 
    </script>
</body>

</html>
```

**输出:**

![](img/a25421604ae4c21fa32f5f8c99daaa3e.png)