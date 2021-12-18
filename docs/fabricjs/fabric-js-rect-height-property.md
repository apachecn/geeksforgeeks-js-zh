# 织物高度属性

> 原文:[https://www . geesforgeks . org/fabric-js-rect-height-property/](https://www.geeksforgeeks.org/fabric-js-rect-height-property/)

在本文中，我们将看到如何使用 **FabricJS** 设置包含画布矩形的对象的高度。画布矩形意味着矩形是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以定制矩形。

为了实现这一点，我们将使用一个名为 **FabricJS** 的 JavaScript 库。导入库之后，我们将在主体标签中创建一个包含矩形的画布块。之后，我们将初始化由 FabricJS 提供的 Canvas 和 Rect 的实例，并使用**高度**属性设置矩形的高度，并在 Canvas 上渲染 Rect，如下例所示。

**语法:**

```
fabric.Rect({
    width: number,
    height: number,
    height: number
});
```

**参数:**该功能接受三个参数，如上所述，描述如下:

*   **宽度:**指定矩形的宽度。
*   **高度:**指定矩形的高度。
*   **高度:**指定物体的高度。

**示例:**本示例使用 FabricJS 设置画布矩形的高度。

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        Fabric.js | Rect height Property
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
            Fabric.js | Rect height Property  
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
            strokeWidth: 3
        }); 

        // Render the Rect in canvas 
        canvas.add(rectangle); 
        canvas.centerObject(rectangle);
    </script> 
</body> 

</html>
```

**输出:**
![](img/9bb458a4ff4d4e7133dc8eb4ee92e668.png)