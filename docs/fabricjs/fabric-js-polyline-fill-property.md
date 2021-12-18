# 织物. js 折线填充属性

> 原文:[https://www . geesforgeks . org/fabric-js-polyline-fill-property/](https://www.geeksforgeeks.org/fabric-js-polyline-fill-property/)

在本文中，我们将看到如何使用 **FabricJS** 设置画布折线的填充颜色。画布折线是指折线是可移动的，可以根据需要进行拉伸。此外，当涉及初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义折线。

为了实现这一点，我们将使用一个名为 **FabricJS** 的 JavaScript 库。导入库后，我们将在包含折线的主体标记中创建一个画布块。之后，我们将初始化由**fabrijs**提供的画布和折线实例，并使用填充属性设置画布折线的填充颜色，并在画布上渲染折线，如下例所示。

**语法:**

```
var polyline = new fabric.Polyline(Points, { 
            fill: string
        }); 

```

**参数:**该功能接受两个参数，如上所述，如下所述–

*   **点:**保存折线所有点的起点和终点坐标。
*   **填充:**指定填充折线的颜色。

**示例:**

## 超文本标记语言

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        Fabric.js | Polyline fill Property 
    </title> 

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
            Fabric.js | Polyline fill Property 
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

        // Initiate a Polyline instance 
        var polyline = new fabric.Polyline([ 
        { x: 200, 
            y: 10  }, 
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
            y: 10  }], { 
            fill: 'green',
        }); 

        // Render the Polyline in canvas 
        canvas.add(polyline); 
    </script> 
</body> 

</html>
```

**输出:**

[![](img/a5afa871fc262c6362416cf9508f2bab.png)](https://media.geeksforgeeks.org/wp-content/uploads/20200817014752/fill.png)