# Fabric.js 折线锁定移动属性

> 原文:[https://www . geesforgeks . org/fabric-js-polyline-lock movementx-property/](https://www.geeksforgeeks.org/fabric-js-polyline-lockmovementx-property/)

在本文中，我们将看到如何使用 FabricJS 锁定画布折线的垂直移动。画布折线是指折线是可移动的，可以根据需要进行拉伸。此外，在初始描边颜色、高度、宽度、填充颜色或描边宽度方面，可以自定义折线。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。导入库后，我们将在包含折线的主体标记中创建一个画布块。之后，我们将初始化 FabricJS 提供的画布和折线实例，并使用 lockMovementX 属性锁定画布折线的水平移动，并在画布上渲染折线，如下例所示。

**语法:**

```
var polyline = new fabric.Polyline(Points, {  
        lockMovementX: Boolean
     });  
```

**参数:**该属性接受如上所述的单个参数，如下所述:

*   **lockMovementX:** 是一个布尔值，指定是否锁定画布的水平移动。

下面的例子说明了 Fabric.js 中的 lockMovementX 属性:

**示例:**

## 超文本标记语言

```
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
            Fabric.js | Polyline lockMovementX Property 
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
            stroke: 'green',  
            strokeWidth: 3,  
            cornerStyle: 'circle',  
            // Disable movement 
            // along the x-axis 
            lockMovementX: true 

        }); 

        // Render the polyline in canvas 
        canvas.add(polyline); 
    </script> 
</body> 

</html>
```

**输出:**

![](img/71ad000cfd98ca4c0132cf5d69705b32.png)