# Fabric.js | Rect moveCursor 属性

> 原文:[https://www . geesforgeks . org/fabric-js-rect-move cursor-property/](https://www.geeksforgeeks.org/fabric-js-rect-movecursor-property/)

在本文中，我们将看到如何使用 FabricJS 设置矩形画布的 **moveCursor** 属性。当我们移动画布对象时，光标将会改变。画布矩形意味着矩形是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以定制矩形。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。导入库之后，我们将在主体标签中创建一个包含矩形的画布块。之后，我们将初始化 FabricJS 提供的 canvas 和 Rectangle 的实例，并使用 **moveCursor** 属性设置 Canvas 矩形的移动光标值，并在 Canvas 上渲染矩形，如下例所示。

**语法:**

```
fabric.Rect({
    width: number,
    height: number,
    moveCursor: string
});
```

**参数:**该功能接受三个参数，如上所述，描述如下:

*   **宽度:**指定矩形的宽度。
*   **高度:**指定矩形的高度。
*   **移动光标:**指定移动画布对象时的光标值。

**示例:**本示例使用 FabricJS 设置对象移动时将起作用的**移动光标**值。

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        Fabric.js | Rect moveCursor Property
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
            Fabric.js | Rect moveCursor Property  
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
            moveCursor: 'pointer'
        }); 

        // Render the Rect in canvas 
        canvas.add(rectangle); 
        canvas.centerObject(rectangle);
    </script> 
</body> 

</html>
```

**输出:**
![](img/2a9633b31c4578a79df9c90069f5d82c.png)