# 织物|三角形 strokeDashArray 属性

> 原文:[https://www . geesforgeks . org/fabric-js-triangle-strokedasharray-property/](https://www.geeksforgeeks.org/fabric-js-triangle-strokedasharray-property/)

在本文中，我们将看到如何使用 FabricJS 设置画布三角形的笔画划线模式。画布三角形是指三角形是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义三角形。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。导入库后，我们将在主体标签中创建一个包含三角形的画布块。之后，我们将初始化 FabricJS 提供的 Canvas 和 Triangle 的实例，并分别使用 stroke 和 **strokeDashArray** 属性设置三角形的笔画颜色和笔画虚线图案，并在 Canvas 上渲染三角形，如下例所示。

**语法:**

```
fabric.Triangle({
    width: number,
    height: number,
    stroke: string,
    strokeDashArray: array
});
```

**参数:**该功能接受三个参数，如上所述，描述如下:

*   **宽度:**指定三角形的宽度。
*   **高度:**指定三角形的高度。
*   **笔画:**指定笔画颜色。
*   **strokeDashArray:** 指定笔画破折号模式。

**示例:**本示例使用 FabricJS 设置画布三角形的描边划线图案。

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        Fabric.js | Triangle strokeDashArray Property
    </title> 

    <!-- Adding the FabricJS library -->
    <script src= 
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js"> 
    </script> 
</head> 

<body> 
    <center>
       <h1 style="color: green;">
        GeeksforGeeks
       </h1>
       <b>
        Fabric.js | Triangle strokeDashArray Property
       </b>
    </center>
    <canvas id="canvas" width="600" height="300"
        style="border:1px solid #000000"> 
    </canvas> 

    <script> 

        // Initiate a Canvas instance 
        var canvas = new fabric.Canvas("canvas"); 

        // Initiate a triangle instance 
        var triangle = new fabric.Triangle({
            width: 300,
            height: 150,
            fill: '',
            stroke: 'green',
            strokeWidth: 3,
            strokeDashArray: [10]
        });

        // Render the Triangle in canvas 
        canvas.add(triangle); 
        canvas.centerObject(triangle);
    </script> 
</body> 

</html>
```

**输出:**
![](img/52dc87e01d4c5ee6c0a2d8dba0eebe74.png)