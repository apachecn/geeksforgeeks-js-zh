# Fabric.js 文本框 originX 属性

> 原文:[https://www . geesforgeks . org/fabric-js-textbox-originx-property/](https://www.geeksforgeeks.org/fabric-js-textbox-originx-property/)

在本文中，我们将看到如何使用 FabricJS 设置 Textbox 画布对象的水平原点。画布文本框意味着文本框是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义文本框。

**进场:**

*   为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript HTML5 画布库。
*   导入库之后，我们将在主体标签中创建一个包含文本框的画布块。
*   之后，我们将初始化由 FabricJS 提供的 Canvas 和 Textbox 的实例，并使用 originX 属性设置 Textbox 的水平转换，并在 Canvas 上呈现 Textbox，如下例所示。

**语法:**

```
fabric.Textbox('text', {
   originX: string
});
```

**参数:**该功能接受如上所述的单个参数，描述如下:

*   **originX:** 指定画布文本框的水平变换。

**示例:**本示例使用 FabricJS 设置画布文本框的水平变换。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js | Textbox originX Property
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
        Fabric.js | Textbox originX Property
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
            originX: "center"
        });

        // Render the Textbox in canvas 
        canvas.add(text);
        //canvas.centerObject(text);
    </script>
</body>

</html>
```

**输出:**

![](img/a33a7c341a79123be007e7d06f9760a7.png)