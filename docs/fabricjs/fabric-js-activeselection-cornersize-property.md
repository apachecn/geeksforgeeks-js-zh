# fabric . js active selection corner size 属性

> 原文:[https://www . geesforgeks . org/fabric-js-activeselection-corner size-property/](https://www.geeksforgeeks.org/fabric-js-activeselection-cornersize-property/)

Fabric.js 是一个用于处理画布的 JavaScript 库。画布**活动选择**是用于创建活动选择实例的 Fabric.js 类之一。画布活动选择意味着活动选择是可移动的，可以根据需要拉伸。在本文中，我们将使用**角尺寸**属性来设置画布的角的尺寸。

**方法:**首先导入 fabric.js 库。导入库后，在主体标签中创建一个包含动态选择的画布块。之后，初始化一个由 Fabric.js 提供的 Canvas 和 ActiveSelection 类的实例，并使用 **cornerSize** 属性设置角的大小。

**语法:**

```html
fabric.ActiveSelection(ActiveSelection, {
  cornerSize: number
});
```

**参数:**该函数采用如上所述的单个参数，描述如下:

*   **角尺寸:**该参数取一个表示角尺寸的数值。

**示例:**本示例使用 FabricJS 设置画布 ActiveSelection 的 cornerSize 属性。

## 超文本标记语言

```html
<!DOCTYPE html>
<html>

<head>
    <!-- FabricJS CDN -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <div style="text-align: center; width: 400px;">
        <h1 style="color: green;">
            GeeksforGeeks
        </h1>

        <b>
            Fabric.js | ActiveSelection cornerSize Property
        </b>
    </div>

    <div style="text-align: center;">
        <canvas id="canvas" width="500" height="500" 
            style="border:1px solid green;">
        </canvas>
    </div>

    <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200327230544/g4gicon.png"
        width="100" height="100"
        id="my-image" style="display: none;">

    <script>
        var canvas = new fabric.Canvas("canvas");

        // Getting the image 
        var img = document.getElementById('my-image');

        // Creating the image instance 
        var geek = new fabric.Image(img, {
        });

        canvas.add(geek);

        var geek = new fabric.IText('GeeksforGeeks', {
        });
        canvas.add(geek);
        canvas.centerObject(geek);

        var gfg = new fabric.ActiveSelection(
            canvas.getObjects(), {
            cornerSize: 30
        });
        canvas.setActiveObject(gfg);
        canvas.requestRenderAll();
        canvas.centerObject(gfg);
    </script>
</body>

</html>
```

**输出:**

![](img/e19383b5a8d1e443204a3931830d878e.png)