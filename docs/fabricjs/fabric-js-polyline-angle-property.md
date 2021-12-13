# 织物. js 折线角度属性

> 原文:[https://www . geesforgeks . org/fabric-js-polyline-angle-property/](https://www.geeksforgeeks.org/fabric-js-polyline-angle-property/)

在本文中，我们将看到如何使用 **FabricJS** 设置画布折线中对象旋转的**角度**。画布折线意味着折线是可移动的，可以根据需要拉伸。此外，在初始描边颜色、高度、宽度、填充颜色或描边宽度方面，可以自定义折线。

为了实现这一点，我们将使用一个名为 **FabricJS** 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个画布块，它将包含我们的折线。之后，我们将初始化 FabricJS 提供的画布和折线实例，并使用 angle 属性将文本旋转到所需的角度，并在折线上渲染画布，如下例所示。

**语法:**

```html
var polyline = new fabric.Polyline(Points, {  
    angle: number
});  
```

**参数:**该属性接受如上所述的单个参数，如下所述:

*   **角度:**指定旋转角度。

以下示例说明了 Fabric.js 中的角度属性:

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
          Fabric.js | Polyline angle Property 
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
            angle: 30 
        }); 

        // Render the polyline in canvas 
        canvas.add(polyline); 
    </script> 
</body> 

</html>
```

**输出:**

![](img/ad9dafa53104c427b0bab17750f165cb.png)