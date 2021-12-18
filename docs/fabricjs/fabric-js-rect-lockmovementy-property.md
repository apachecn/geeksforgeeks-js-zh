# 织物|直锁运动属性

> 原文:[https://www . geesforgeks . org/fabric-js-rect-lock movementy-property/](https://www.geeksforgeeks.org/fabric-js-rect-lockmovementy-property/)

在本文中，我们将看到如何使用 FabricJS 锁定画布矩形的垂直移动。画布矩形意味着矩形是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以定制矩形。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。导入库之后，我们将在主体标签中创建一个包含矩形的画布块。之后，我们将初始化由 FabricJS 提供的 canvas 和 Rect 的实例，并使用 **lockMovementY** 属性锁定 Canvas 矩形的垂直移动，并在 Canvas 上渲染 Rect，如下例所示。

**语法:**

```
fabric.Rect({
    width: number,
    height: number,
    lockMovementY: Boolean
});
```

**参数:**该功能接受三个参数，如上所述，描述如下:

*   **宽度:**指定矩形的宽度。
*   **高度:**指定矩形的高度。
*   **lockMovementY:** 指定是否锁定画布的垂直移动。

**示例:**本示例使用 FabricJS 锁定画布状矩形的垂直移动，如下所示。

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        Fabric.js | Rect lockMovementY Property
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
            Fabric.js | Rect lockMovementY Property  
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
            lockMovementY: true
        }); 

        // Render the Rect in canvas 
        canvas.add(rectangle); 
        canvas.centerObject(rectangle);
    </script> 
</body> 

</html>
```

**输出:**
![](img/92e6f6a437e3dc38a8ee100f0442a085.png)