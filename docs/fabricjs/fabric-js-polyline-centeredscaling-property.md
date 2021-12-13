# 织物. js 折线中心缩放属性

> 原文:[https://www . geesforgeks . org/fabric-js-polyline-centered scaling-property/](https://www.geeksforgeeks.org/fabric-js-polyline-centeredscaling-property/)

在本文中，我们将看到如何使用 FabricJS 启用画布折线的居中缩放。画布意味着折线是可移动的，可以根据需要拉伸。此外，在初始描边颜色、填充颜色、描边宽度或半径方面，可以自定义多段线。

为了实现这一点，我们将使用一个名为 **FabricJS** 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个画布块，其中将包含我们的折线。之后，我们将初始化由 FabricJS 提供的画布和折线实例，并使用**中心缩放**属性启用画布折线的中心缩放，并在画布上渲染折线，如下所示。

**语法:**

```html
var polyline = new fabric.Polyline(Points, {  
    centeredScaling: boolean
});  
```

**参数:**该属性接受如上所述的单个参数，如下所述:

*   **居中缩放:**指定是启用还是禁用居中缩放。

以下示例说明了 Fabric.js 中的中心缩放属性:

**示例:**

## 超文本标记语言

```html
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
            Fabric.js | Polyline centeredScaling Property 
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

        // Initiate a polyline instance 
        var polyline = new fabric.Polyline([ 
        { x: 200, 
            y: 10 }, 
        {x: 250, 
            y: 50 
        }, { 
            x: 250, 
            y: 180 
        }, { 
            x: 150, 
            y: 180 
        }, { 
            x: 150, 
            y: 50 
        }, { 
            x: 200, 
            y: 10 }], { 
            centeredScaling: true ,
            borderScaleFactor: 3 
        }); 

        // Render the polyline in canvas 
        canvas.add(polyline); 
    </script> 
</body> 

</html>
```

**输出:**

![](img/37231ee4e61fbe9af647b953c2d5304e.png)