# Fabric.js 折线悬停光标属性

> 原文:[https://www . geesforgeks . org/fabric-js-polyline-悬停光标-property/](https://www.geeksforgeeks.org/fabric-js-polyline-hovercursor-property/)

在本文中，我们将使用 FabricJS 查看折线画布的悬停光标属性。画布折线是指折线是可移动的，可以根据需要进行拉伸。此外，在初始描边颜色、高度、宽度、填充颜色或描边宽度方面，可以自定义折线。

**方法:**为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。导入库后，我们将在包含折线的主体标记中创建一个画布块。之后，我们将初始化 FabricJS 提供的画布和折线实例，并使用悬停光标属性设置画布折线的悬停光标，并在画布上渲染折线，如下例所示。

**语法:**

```
var polyline = new fabric.Polyline(Points, {  
    hoverCursor: string
});  
```

**参数:**该属性接受如上所述的单个参数，如下所述:

*   **悬停光标:**指定悬停光标的值。

以下示例说明了在 Fabric.js 中使用悬停光标属性:

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
            Fabric.js | Polyline hoverCursor Property 
        </b>
    </div>

    <canvas id="canvas" width="600" height="200" 
        style="border:1px solid #000000;"> 
    </canvas>

    <script>
        // Initiate a Canvas instance 
        var canvas = new fabric.Canvas("canvas");

        // Initiate a polyline instance 
        var polyline = new fabric.Polyline([{
            x: 200,
            y: 10
        }, {
            x: 250,
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
            y: 10
        }], {
            stroke: 'green',
            strokeWidth: 3,
            cornerStyle: 'circle',
            hoverCursor: 'pointer',
        });

        // Render the polyline in canvas 
        canvas.add(polyline);
    </script>
</body>

</html>
```

**输出:**

![](img/13f4047117a6243d34840d69a488bafd.png)