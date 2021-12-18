# fabric . js Textbox lock movementx 属性

> 原文:[https://www . geesforgeks . org/fabric-js-textbox-lock movementx-property/](https://www.geeksforgeeks.org/fabric-js-textbox-lockmovementx-property/)

在本文中，我们将看到如何使用 Fabric.js 锁定画布 Textbox 的水平移动。Fabric.js 中的 Textbox 是可移动的，可以根据需要进行拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义文本框。

为了实现这一点，我们将使用一个名为 Fabric.js 的 JavaScript 库。导入库后，我们将在主体标签中创建一个包含 Textbox 的画布块。之后，我们将初始化 Fabric.js 提供的 canvas 和 Textbox 的实例，使用 lockMovementX 属性锁定 canvas Textbox 的水平移动，并在 Canvas 上呈现 Textbox，如下例所示。

**语法:**

```
fabric.Textbox('text', {
   lockMovementX: boolean
});
```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **lockMovementX:** 指定是否锁定画布的水平移动。

**示例:**该示例使用 Fabric.js 锁定文本框的水平移动，如下所示。

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
        Fabric.js | Textbox lockMovementX Property
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
            width: 500,
            lockMovementX: true
        });

        // Render the Textbox in canvas 
        canvas.add(text);
        canvas.centerObject(text);
    </script>
</body>
</html>
```

**输出:**

![](img/80159af2b9f29b5b9908c754d3f50ce6.png)