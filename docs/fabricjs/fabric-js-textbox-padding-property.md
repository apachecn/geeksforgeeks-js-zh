# 织物. js 文本框填充属性

> 原文:[https://www . geesforgeks . org/fabric-js-textbox-padding-property/](https://www.geeksforgeeks.org/fabric-js-textbox-padding-property/)

在本文中，我们将看到如何使用 FabricJS 更改对象和控制画布文本框边框之间的填充。画布文本框意味着文本框是可移动的，可以根据需要进行拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义文本框。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。导入库后，我们将在主体标签中创建一个包含文本框的画布块。之后，我们将初始化由 FabricJS 提供的 Canvas 和 Textbox 的实例，并使用 padding 属性更改对象和 Textbox 的控制边框之间的填充，并在 Canvas 上呈现 Textbox，如下例所示。

**语法:**

```
fabric.Textbox('text', {
   padding: number
});
```

**参数:**该函数接受一个参数，如上所述，如下所述:

*   **填充:**指定对象和控制边框之间的填充。

**示例:**本示例使用 FabricJS 更改画布文本框的对象和控制边框之间的填充。请注意，您必须单击对象才能看到填充。

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
    <h1 style="color: green;">
        GeeksforGeeks
    </h1>

    <h3>
        Fabric.js | Textbox padding Property
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
            padding: 50
        });

        // Render the Textbox in canvas 
        canvas.add(text);
        canvas.centerObject(text);
    </script>
</body>

</html>
```

**输出:**

![](img/5568ff5c7f9e4ba97a2bfbe0cb29192f.png)