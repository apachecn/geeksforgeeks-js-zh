# 织物. js 多边形可见属性

> 原文:[https://www . geesforgeks . org/fabric-js-polygon-visible-property/](https://www.geeksforgeeks.org/fabric-js-polygon-visible-property/)

在本文中，我们将看到如何使用 FabricJS 设置画布多边形的可见性。画布意味着多边形是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、填充颜色、笔画宽度或半径时，可以自定义椭圆。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在包含我们的多边形的主体标签中创建一个画布块。之后，我们将初始化由 FabricJS 提供的 canvas 和 Polygon 的实例，并使用 visible 属性设置 canvas Polygon 的可见性，并在 Canvas 上渲染 Polygon，如下例所示。

**语法:**

```
fabric.Polygon([  
       { x: pixel, y: pixel },  
       { x: pixel, y: pixel },  
       { x: pixel, y: pixel},  
       { x: pixel, y: pixel},  
       { x: pixel, y: pixel }],
       {
               visible: boolean
       });
```

**参数:**该属性接受如上所述的单个参数，如下所述:

*   **可见:**指定多边形的可见性。

**注意:**尺寸像素是必须创建的多边形。

下面的例子说明了织物。JavaScript 中的多边形可视化:

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
            Fabric.js | Polygon visible Property 
        </b> 
        </div> 
    <canvas id="canvas"
            width="600"
            height="200"
            style="border:1px solid #000000;"> 
    </canvas> 

    <script> 

        // Initiate a Canvas instance 
        var canvas = new fabric.Canvas("canvas"); 

        // Initiate a polygon instance 
        var polygon = new fabric.Polygon([ 
        { x: 295, y: 10 }, 
        { x: 235, y: 198 }, 
        { x: 385, y: 78}, 
        { x: 205, y: 78}, 
        { x: 355, y: 198 }]
        visible: false,); 

        // Render the polygon in canvas 
        canvas.add(polygon); 
    </script> 
</body> 

</html>
```

**输出:**

![](img/853b0ef68c23456b51fc3b8587f30375.png)