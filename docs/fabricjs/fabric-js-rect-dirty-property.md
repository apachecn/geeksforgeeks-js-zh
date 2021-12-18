# 织物|直脏属性

> 原文:[https://www . geesforgeks . org/fabric-js-rect-dirty-property/](https://www.geeksforgeeks.org/fabric-js-rect-dirty-property/)

在本文中，当我们将 dirty 属性设置为 true 时，对象缓存将在下一次使用 FabricJS 对画布矩形进行渲染调用时重新呈现。画布矩形意味着矩形是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以定制矩形。

**方法:**为了使其成为可能，我们将使用一个名为 FabricJS 的 JavaScript 库。导入库之后，我们将在主体标签中创建一个包含矩形的画布块。之后，我们将初始化由 FabricJS 提供的 canvas 和 rectangle 的实例，并设置 canvas rectangle 的脏属性，它将在 Canvas 上呈现 Rectangle，如下例所示。

**语法:**

```
fabric.Rect({
    width: number,
    height: number,
    dirty: Boolean
});
```

**参数:**该功能接受三个参数，如上所述，描述如下:

*   **宽度:**指定矩形的宽度。
*   **高度:**指定矩形的高度。
*   **dirty:** 指定下次渲染调用时是否重新渲染对象缓存。

**示例:**本示例使用 FabricJS 在画布矩形上设置 dirty 属性，如下所示。

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        Fabric.js | Rect dirty Property
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
            stroke: 'green',
            strokeWidth: 3,
            cornerStyle: 'circle',
            dirty: false
        }); 

        // Render the Rect in canvas 
        canvas.add(rectangle); 
        canvas.centerObject(rectangle);
    </script> 
</body> 

</html>
```

**输出:**
![](img/43de5c3e530d6090de53638dce88860c.png)