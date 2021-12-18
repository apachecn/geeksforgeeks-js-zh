# Fabric.js 文本框绝对定位属性

> 原文:[https://www . geesforgeks . org/fabric-js-textbox-absoluteposited-property/](https://www.geeksforgeeks.org/fabric-js-textbox-absolutepositioned-property/)

在本文中，我们将看到如何使用 Fabric.js 设置文本框的绝对位置。只有当对象被用作剪辑路径时，它才有意义。Fabric.js 中的 Textbox 是可移动的，可以根据需要进行拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义文本框。

为了实现这一点，我们将使用一个名为 Fabric.js 的 JavaScript 库。在导入库之后，我们将在主体标签中创建一个包含 Textbox 的画布块。之后，我们将初始化由 Fabric.js 提供的 Canvas 和 Textbox 的实例，并使用 absolutePositioned 属性设置 canvas Textbox 的绝对位置。

**语法:**

```
fabric.Textbox('text', {
    absolutePositioned: boolean
});
```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **绝对定位:**指定文本框是否绝对定位。

**示例:**本示例使用 Fabric.js 设置 Textbox 的绝对位置。

## 超文本标记语言

```
<html>
<head>
    <!-- Adding the FabricJS library -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/4.3.0/fabric.min.js">
    </script>
</head>
<body>
    <h1 style="color: green;">
        GeeksforGeeks
    </h1>
    <h3>
        Fabric.js | Textbox absolutePositioned Property
    </h3>
    <canvas id="canvas" width="600" height="300" 
        style="border:1px solid #000000">
    </canvas>
    <script>
        // Initiate a Canvas instance 
        var canvas = new fabric.Canvas("canvas");

        // Create a new Textbox instance 
        var text = new fabric.Textbox(
            'A Computer Science Portal', {
            width: 450,
            absolutePositioned: true
        });

        // Render the Textbox in canvas 
        canvas.add(text);
        canvas.centerObject(text);
    </script>
</body>
</html>
```

**输出:**

![](img/4279068f45c5ad08d2a74b00d0ff44ce.png)