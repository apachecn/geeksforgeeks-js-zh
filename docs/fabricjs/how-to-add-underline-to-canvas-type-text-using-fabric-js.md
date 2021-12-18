# 如何使用 Fabric.js 给画布型文本添加下划线？

> 原文:[https://www . geesforgeks . org/如何在画布上添加下划线-文字-使用织物-js/](https://www.geeksforgeeks.org/how-to-add-underline-to-canvas-type-text-using-fabric-js/)

在本文中，我们将看到如何使用 FabricJS 为类似画布的文本添加下划线。画布意味着书写的文本是可移动的、可旋转的、可调整大小的，并且可以拉伸。但是在这篇文章中，我们将为文本添加下划线。此外，文本本身不能像文本框一样编辑。
**方法:**为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个包含文本的*画布*块。之后，我们将初始化 FabricJS 提供的 Canvas 和 Text 的实例，并使用**下划线**属性添加下划线，并在文本上呈现 Canvas，如下例所示。

**语法:**

```
 fabric.text(text :string, underline: boolean); 
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **文本:**指定文本。
*   **下划线:**指定是否加下划线。

**程序:**这个例子使用 FabricJS 为画布状的文本添加下划线，如下所示。\

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        How to add underline to canvas-type
        text using Fabric.js ?
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

        // Create a new Text instance
        var text = new fabric.Text('GeeksforGeeks', {
            underline: true
        });

        // Render the text on Canvas
        canvas.add(text);
    </script>
</body>

</html>
```

**输出:**

![](img/46ba7a422a0dfc9f47af08bc2a96880d.png)