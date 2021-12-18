# fabric . js Textbox minscalelint 属性

> 原文:[https://www . geeksforgeeks . org/fabric-js-textbox-minscalelimit-property/](https://www.geeksforgeeks.org/fabric-js-textbox-minscalelimit-property/)

在本文中，我们将看到如何使用 FabricJS 设置画布 Textbox 的最小允许比例限制，以便保持对象的纵横比。画布意味着文本框是可移动的，可以根据需要拉伸。此外，文本框可以自定义初始笔画颜色、填充颜色、笔画宽度或半径。

**进场:**

*   为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。
*   在使用 CDN 导入库之后，我们将在包含我们的 Textbox 的主体标签中创建一个画布块。
*   之后，我们将初始化由 FabricJS 提供的 canvas 和 Textbox 的实例，并使用 minScaleLimit 属性设置 canvas Textbox 的最小允许比例限制，并在 Canvas 上呈现 Textbox，如下例所示。

**语法:**

```
fabric.Textbox('text', {
   minScaleLimit: number
});
```

**参数:**该函数接受一个参数，如上所述，如下所述:

*   **明刻度极限:**指定最小刻度极限。

**示例:**本示例使用 FabricJS 设置画布文本框的最小允许比例限制。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js | Textbox minScaleLimit Property
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
        Fabric.js | Textbox minScaleLimit Property
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
            minScaleLimit: 2
        });

        // Render the Textbox in canvas 
        canvas.add(text);
        canvas.centerObject(text);
    </script>
</body>

</html>
```

**输出:**

![](img/90ed285d16586f13333f286d94dddf92.png)