# Fabric.js 折线可选属性

> 原文:[https://www . geesforgeks . org/fabric-js-polyline-selected-property/](https://www.geeksforgeeks.org/fabric-js-polyline-selectable-property/)

在本文中，我们将看到如何使用 **FabricJS** 设置画布折线的可选择性。画布折线是指折线是可移动的，可以根据需要进行拉伸。此外，当初始*笔画颜色、形状、填充颜色、*或*笔画宽度时，可以自定义折线。*

为了实现这一点，我们将使用一个名为 **FabricJS** 的 JavaScript 库。导入库后，我们将在包含折线的主体标记中创建一个画布块。之后，我们将初始化 FabricJS 提供的画布和折线实例，并使用*可选*属性设置折线的可选性，并在画布上渲染折线，如下例所示。

**语法:**

```
var polyline = new fabric.Polyline(Points, {  
   selectable: boolean
  });  
```

**参数:**该属性接受一个参数，如上所述，如下所述。

*   **可选:**指定画布是否可选。

**示例:**以下示例说明了 **Fabric.js** 中的*可选*属性

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
            Fabric.js | Polyline selectable Property 
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
            selectable: false   

        }); 

        // Render the polyline in canvas 
        canvas.add(polyline); 
    </script> 
</body> 

</html>
```

**输出:**

![](img/dc4acdbb8ed57b9f2749398dbaa497ff.png)