# 如何使用 Fabric.js 仅移除画布类型文本的旋转控件？

> 原文:[https://www . geesforgeks . org/how-to-remove-only-rotation-controls-of-a-canvas-type-text-use-fabric-js/](https://www.geeksforgeeks.org/how-to-remove-only-rotation-controls-of-a-canvas-type-text-using-fabric-js/)

在本文中，我们将看到如何使用 FabricJS 仅移除画布状文本的旋转控件。画布意味着书写的文本是可移动的，可以根据需要拉伸，但我们将删除旋转控件，使其不能旋转，只能移动和调整大小。此外，文本本身不能像文本框一样编辑。
**方法:**为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个包含文本的*画布*块。之后，我们将初始化 FabricJS 提供的 Canvas 和 Text 实例，并使用 **hasRotatingPoint** 属性仅移除旋转控件，并在 Text 上渲染 Canvas，如下例所示。

**语法:**

```
 fabric.Text(text, hasRotatingPoint: boolean); 
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **文本:**指定要写入的文本。
*   **有旋转点:**指定是启用还是禁用旋转控制，默认启用。

**程序:**我们可以使用 FabricJS 只移除画布状文本的旋转控制，如下所示。请注意，您必须单击文本来查看其控件是否存在。

## 超文本标记语言

```
<!DOCTYPE hyml>
<html>

<head>
    <title>
        How to remove only rotating controls of
        a canvas-type text with JavaScript?
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
            hasRotatingPoint: false
        });

        // Render the Textboxes on Canvas
        canvas.add(text);
    </script>
</body>

</html>
```

**输出:**

![](img/8992881e63c0b29296f46ccf55049cec.png)