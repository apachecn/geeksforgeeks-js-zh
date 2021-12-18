# fabric . js | Rect background color 属性

> 原文:[https://www . geesforgeks . org/fabric-js-rect-background color-property/](https://www.geeksforgeeks.org/fabric-js-rect-backgroundcolor-property/)

在本文中，我们将创建如何使用 FabricJS 更改画布矩形的背景颜色。画布矩形意味着矩形是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以定制矩形。

**方法:**为了使其成为可能，我们将使用一个名为 FabricJS 的 JavaScript 库。导入库之后，我们将在主体标签中创建一个包含矩形的画布块。之后，我们将初始化由 FabricJS 提供的 canvas 和 Rect 的实例，并使用 background color 属性更改 canvas Rect 的背景颜色，并在 Canvas 上进行渲染，如下例所示。

**语法:**

```
fabric.Rect({
    width: number,
    height: number,
    backgroundColor: string
}); 
```

**参数:**该功能接受三个参数，如上所述，描述如下:

*   **宽度:**指定矩形的宽度。
*   **高度:**指定矩形的高度。
*   **backgroundColor:** 指定背景颜色。

**示例:**本示例使用 FabricJS 更改 Rect 画布的背景颜色。

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        Fabric.js | Rect backgroundColor Property
    </title> 

    <!-- Adding the FabricJS library -->
    <script src= 
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js"> 
    </script> 
</head> 

<body> 
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
            stroke: 'black', 
            strokeWidth: 3,
            backgroundColor: 'green'
        }); 

        // Render the Rect in canvas 
        canvas.add(rectangle); 
        canvas.centerObject(rectangle);
    </script> 
</body> 

</html>
```

![](img/9140394a95dc0f3eabd493dbc1447c30.png)