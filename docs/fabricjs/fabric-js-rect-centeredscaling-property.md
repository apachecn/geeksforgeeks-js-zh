# 织物|矩形中心缩放属性

> 原文:[https://www . geesforgeks . org/fabric-js-rect-centered scaling-property/](https://www.geeksforgeeks.org/fabric-js-rect-centeredscaling-property/)

在本文中，我们将看到如何使用 FabricJS 启用画布矩形的居中缩放。画布矩形意味着矩形是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以定制矩形。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。导入库之后，我们将在主体标签中创建一个包含矩形的画布块。之后，我们将初始化 FabricJS 提供的 canvas 和 Rectangle 实例，并使用**中心缩放**属性启用 Canvas 矩形的中心缩放，并在 Canvas 上渲染 Rect，如下所示。

**语法:**

```
fabric.Rect({
    width: number,
    height: number,
    centeredScaling: boolean
}); 
```

**参数:**该函数接受三个参数，如上所述，如下所述:

*   **宽度:**此参数定义矩形的宽度。
*   **高度:**此参数定义矩形的高度。
*   **居中缩放:**此参数定义是启用还是禁用居中缩放。

**示例:**该示例使用 FabricJS 来启用画布状矩形的居中缩放，如下所示。在启用居中缩放后，尝试缩放对象，当您缩放它时，它将从四面进行缩放。

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        Fabric.js | Rect centeredScaling Property
    </title> 

    <!-- Adding the FabricJS library -->
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
            Fabric.js | Rect centeredScaling Property
          </b>
    </div>
    <canvas id="canvas" width="600" height="200"
        style="border:1px solid #000000"> 
    </canvas> 

    <script> 

        // Initiate a Canvas instance 
        var canvas = new fabric.Canvas("canvas"); 

        // Initiate a Rect instance 
        var rectangle = new fabric.Rect({ 
            width: 200,
            height: 100,
            fill: '', 
            stroke: 'green',
            strokeWidth: 3,
            centeredScaling: true
        }); 

        // Render the Rect in canvas 
        canvas.add(rectangle); 
        canvas.centerObject(rectangle);
    </script> 
</body> 

</html>
```

**输出:**
![](img/f0050f7394c2126a45c05be0d0120a03.png)