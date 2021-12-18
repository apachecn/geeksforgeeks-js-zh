# Fabric.js 文本框 strokeDashOffset 属性

> 原文:[https://www . geesforgeks . org/fabric-js-textbox-strokedashoffset-property/](https://www.geeksforgeeks.org/fabric-js-textbox-strokedashoffset-property/)

在本文中，我们将看到如何使用 **FabricJS** 设置画布 Textbox 的笔画偏移。画布文本框意味着文本框是可移动的，可以根据需要进行拉伸。此外，文本框可以自定义初始*笔画颜色、高度、宽度、填充颜色、*或*笔画宽度。*

为了实现这一点，我们将使用一个名为 **FabricJS** 的 JavaScript 库。导入库后，我们将在主体标签中创建一个包含文本框的画布块。之后，我们将初始化 **FabricJS** 提供的 canvas 和 textbox 的实例，并使用 *stroke* 属性创建一个笔画，并进一步使用 *strokeDashOffset* 属性添加笔画偏移，并在 Textbox 上渲染 Canvas，如下例所示。

**语法:**

```
fabric.Textbox('text', {
   strokeDashOffset: number
});
```

**参数:**该函数接受一个参数，如上所述，如下所述。

*   **strokeDashOffset:** 指定笔画的偏移量。

**示例:**本示例使用**fabrijs**库设置画布文本框的笔画虚线偏移，如下所示。

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
        Fabric.js | Textbox strokeDashOffset Property
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
            strokeDashOffset: 10,
            stroke: 'green'
        });

        // Render the Textbox in canvas 
        canvas.add(text);
        canvas.centerObject(text);
    </script>
</body>

</html>
```

**输出:**

![](img/cadf11189278d8e519a220b7ed2f59b3.png)

![](img/86dc7707a84939a22daac7a329fe3310.png)