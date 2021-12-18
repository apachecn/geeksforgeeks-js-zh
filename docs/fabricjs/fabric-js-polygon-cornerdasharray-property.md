# Fabric.js 多边形角点阵列属性

> 原文:[https://www . geesforgeks . org/fabric-js-polygon-cornerdasharray-property/](https://www.geeksforgeeks.org/fabric-js-polygon-cornerdasharray-property/)

在本文中，我们将看到如何使用 **FabricJS** 设置画布多边形控制角的虚线图案。画布多边形意味着多边形是可移动的，可以根据需要拉伸。此外，多边形可以在初始笔画颜色、高度、宽度、填充颜色或笔画宽度方面进行自定义。

为了实现这一点，我们将使用一个名为 **FabricJS** 的 JavaScript 库。导入库之后，我们将在包含多边形的主体标签中创建一个画布块。之后，我们将初始化由**fabrijs**提供的画布和多边形的实例，并使用 **cornerDashArray** 属性设置控制画布多边形的角的虚线图案，并在画布上渲染多边形，如下例所示。

**语法:**

```
fabric.Polygon([ 
        { x: pixel, y: pixel }, 
        { x: pixel, y: pixel }, 
        { x: pixel, y: pixel }, 
        { x: pixel, y: pixel }, 
        { x: pixel, y: pixel }],
        {
                cornerDashArray: array
        });
```

**参数:**该属性接受如上所述的单个参数，如下所述:

*   **角点阵列:**此参数定义控制角点的虚线图案。

以下示例说明了**织物。JavaScript 中的**多边形**角数组**属性:

**示例:** 该示例使用 FabricJS 设置一个虚线模式来控制画布状矩形的角，如下所示。你必须点击多边形对象才能看到控制角的虚线图案。

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
            Fabric.js | Polygon cornerDashArray Property 
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
                cornerDashArray: [5]   
        }); 

        // Render the polygon in canvas 
        canvas.add(polygon); 
    </script> 
</body> 

</html>
```

**输出:**

![](img/0403d56794c22476ff0a1eb381d29133.png)