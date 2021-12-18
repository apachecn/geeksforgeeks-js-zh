# 织物. js 文本框不透明度属性

> 原文:[https://www . geesforgeks . org/fabric-js-textbox-不透明度-property/](https://www.geeksforgeeks.org/fabric-js-textbox-opacity-property/)

在本文中，我们将看到如何使用 FabricJS 设置文本框画布的不透明度。画布文本框意味着文本框是可移动的，可以根据需要进行拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义文本框。

**进场:**

*   为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。
*   导入库后，我们将在主体标签中创建一个包含文本框的画布块。
*   之后，我们将初始化由 FabricJS 提供的 Canvas 和 Textbox 的实例，并使用不透明度属性设置 Textbox 的不透明度，并在 Canvas 上呈现 Textbox，如下例所示。

**语法:**

```
fabric.Textbox('text', {
   opacity: number
});
```

**参数:**该功能接受如上所述的单个参数，描述如下:

*   **不透明度:**指定画布文本框的不透明度。

**示例:**本示例使用 FabricJS 设置画布文本框的不透明度。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js | Textbox opacity Property
    </title>

    <!-- Adding the FabricJS library -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <h1 style="color: green;">
        GeeksforGeeks
    </h1>

    <h3>
        Fabric.js | Textbox opacity Property
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
            opacity: 0.5
        });

        // Render the Textbox in canvas 
        canvas.add(text);
        canvas.centerObject(text);
    </script>
</body>

</html>
```

**输出:**

![](img/5963c094336b9448dca14b2230806690.png)