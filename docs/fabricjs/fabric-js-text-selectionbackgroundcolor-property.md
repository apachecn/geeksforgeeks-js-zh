# fabric . js | Text selection background color 属性

> 原文:[https://www . geesforgeks . org/fabric-js-text-selectionbackgroundcolor-property/](https://www.geeksforgeeks.org/fabric-js-text-selectionbackgroundcolor-property/)

在本文中，我们将看到如何使用 FabricJS 更改文本画布的活动背景颜色。画布意味着书写的文本是可移动的、可旋转的、可调整大小的，并且可以拉伸。但是在本文中，我们将更改活动背景颜色。此外，文本本身不能像文本框一样编辑。

**方法:**为了使其成为可能，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个包含文本的*画布*块。之后，我们将初始化 FabricJS 提供的 Canvas 和 Text 实例，并使用 **selectionBackgroundColor** 属性来更改活动背景颜色，并在 Text 上渲染 Canvas，如下例所示。

**语法:**

```
 fabric.Text(text, selectionBackgroundColor: string); 
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **文本:**指定要写入的文本。
*   **selectionBackgroundColor:**指定活动时背景的颜色。

**程序:**本示例使用 FabricJS 更改文本画布的活动背景颜色。请注意，我们必须点击文本才能看到活动的背景颜色。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js | Text selectionBackgroundColor Property
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

        // Create a new instace of Canvas
        var canvas = new fabric.Canvas("canvas");

        // Create a new Text instance
        var text = new fabric.Text('GeeksforGeeks', {
            selectionBackgroundColor: 'green'
        });

        // Render the text on Canvas
        canvas.add(text);
    </script>
</body>

</html>
```

**输出:**
![](img/7cd5b516a99f8e94b0ee0e7652e5c77e.png)