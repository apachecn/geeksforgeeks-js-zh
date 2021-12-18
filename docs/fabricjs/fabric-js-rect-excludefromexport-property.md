# fabric . js Rect exclude defromexport 属性

> 原文:[https://www . geeksforgeeks . org/fabric-js-rect-excludefromexport-property/](https://www.geeksforgeeks.org/fabric-js-rect-excludefromexport-property/)

在本文中，我们将看到如何使用 FabricJS 禁用画布 Rect 的导出。画布矩形意味着矩形是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义矩形。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。导入库之后，我们将在主体标签中创建一个包含 Rect 的画布块。之后，我们将初始化由 FabricJS 提供的 canvas 和 Rect 的实例，并使用 excludeFromExport 属性禁用 canvas Rect 的 Canvas click move 属性，并在 Canvas 上渲染 Rect，如下所示。

**语法:**

```
fabric.Rect({
    width: number,
    height: number,
    excludeFromExport: boolean 
});
```

**参数:**该属性接受如上所述的单个参数，如下所述:

*   **exclude defromexport:**当` true '时，对象不在 OBJECT/JSON 中导出。

下面的例子说明了 Fabric.js 中的 excludeFromExport:

**示例:**

## 超文本标记语言

```
<!DOCTYPE html> 
<html> 

<head> 
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
            Fabric.js | Rect excludeFromExport Property 
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
            excludeFromExport: 'false'
        }); 

        // Render the Rect in canvas 
        canvas.add(rectangle); 
        canvas.centerObject(rectangle); 
    </script> 
</body> 

</html>
```

**输出:**

![](img/8405a754a4ec51ee4c300940ca5ece1d.png)