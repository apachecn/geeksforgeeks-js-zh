# 织物. js 多边形边界颜色属性

> 原文:[https://www . geesforgeks . org/fabric-js-polygon-border color-property/](https://www.geeksforgeeks.org/fabric-js-polygon-bordercolor-property/)

在本文中，我们将看到如何使用 **FabricJS** 绘制一个带边框的彩色画布多边形。画布多边形意味着多边形是可移动的，可以根据需要拉伸。此外，多边形可以在初始笔画颜色、高度、宽度、填充或笔画宽度方面进行自定义。

**方法:**为了实现这一点，我们将使用一个名为**的 JavaScript 库。导入库后，我们将在包含多边形的主体标签中创建一个画布块。之后，我们将初始化由**fabrijs**提供的画布和多边形的实例，并使用 borderColor 属性启用画布多边形的 borderColor，并在画布上渲染多边形，如下所示。**

**语法:**

```
fabric.Polygon([ 
        { x: pixel, y: pixel }, 
        { x: pixel, y: pixel }, 
        { x: pixel, y: pixel}, 
        { x: pixel, y: pixel}, 
        { x: pixel, y: pixel }],
        {
                borderColor: string
        });
```

**参数:**该属性接受如上所述的单个参数，如下所述:

*   **边框颜色:**此参数定义多边形的边框颜色。

下面的例子说明了**织物。JS**T2【多边形边界颜色】属性在 JavaScript 中:

**示例:**在本例中，我们将多边形的 borderColor 属性设置为**紫色**。

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
            Fabric.js | Polygon borderColor Property 
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
        { x: 355, y: 198 }], { 
            stroke: 'green',  
            strokeWidth: 3,  
            cornerColor: 'blue',  
            borderColor: 'purple' 
        }); 

        // Render the polygon in canvas 
        canvas.add(polygon); 
    </script> 
</body> 

</html>
```

**输出:**

![](img/e0f394fb67f6e5408d1e0fccdd5c269d.png)