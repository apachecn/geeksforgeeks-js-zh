# 如何使用 Fabric.js 在画布上创建文本？

> 原文:[https://www . geesforgeks . org/如何使用 fabric-js 创建画布上的文本/](https://www.geeksforgeeks.org/how-to-create-text-on-canvas-using-fabric-js/)

在本文中，我们将看到如何使用 FabricJS 在画布上创建文本。画布上的文本意味着书写的文本是可移动的，可以根据需要拉伸。此外，文本本身不能像文本框一样编辑。

**方法:**为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个包含文本的*画布*块。在此之后，我们将初始化 FabricJS 提供的 Canvas 和 Text 实例，并在 Text 上呈现 Canvas，如下例所示。

**语法:**

```html
 fabric.Text(text, options); 
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **文本:**指定要写入的文本。
*   **选项:**指定要应用的附加选项。

**示例:**本示例使用 FabricJS 在画布上创建简单的可编辑文本。

## 超文本标记语言

```html
<!DOCTYPE html>
<html>

<head>
    <title>
        How to Create Text on
        Canvas using Fabric.js?
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
            fill: 'green'
        });

        // Render the Text on Canvas
        canvas.add(text);
    </script>
</body>

</html>
```

**输出:**

![](img/baedc9d382729ae9d5fe7d1e01477952.png)