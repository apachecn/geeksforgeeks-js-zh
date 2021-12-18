# 如何使用 Fabric.js 移除文本画布的控件？

> 原文:[https://www . geesforgeks . org/如何移除文本画布控件-使用织物-js/](https://www.geeksforgeeks.org/how-to-remove-controls-of-a-text-canvas-using-fabric-js/)

在本文中，我们将看到如何使用 FabricJS 移除文本画布的控件。画布意味着书写的文本是可移动的，可以根据需要拉伸，但我们将删除控件，使其不能调整大小或旋转，而只能移动。此外，文本本身不能像文本框一样编辑。
**方法:**为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个包含文本的*画布*块。之后，我们将初始化 FabricJS 提供的 Canvas 和 Text 的实例，并使用 **hasControls** 属性移除控件并在 Text 上呈现 Canvas，如下例所示。

**语法:**

```
fabric.Text(text, hasControls: boolean); 
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **文本:**指定要写入的文本。
*   **hasControls:** 指定是启用还是禁用控件，默认启用。

**程序:**本示例使用 FabricJS 移除文本画布的控件。请注意，您必须单击文本来查看其控件是否存在。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        How to remove controls of a
        text canvas using Fabric.js?
    </title>

    <!-- Loading the FabricJS library -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <canvas id="canvas" width="600" height="200"
        style="border:1px solid #000000;">
    </canvas>

    <script>

        // Create a new instance of Canvas
        var canvas = new fabric.Canvas("canvas");

        // Create a new Textbox instance
        var text = new fabric.Text('GeeksforGeeks', {
            hasControls: false
        });

        // Render the Textboxes on Canvas
        canvas.add(text);
    </script>
</body>

</html>
```

**输出:**

![](img/11d2fbacfe593a3d03400fe835b8f9bb.png)