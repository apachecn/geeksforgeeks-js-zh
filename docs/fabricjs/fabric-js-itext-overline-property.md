# Fabric.js Itext 跨线属性

> 原文:[https://www . geesforgeks . org/fabric-js-itext-overline-property/](https://www.geeksforgeeks.org/fabric-js-itext-overline-property/)

Fabric.js 是一个用于处理画布的 JavaScript 库。画布 Itext 是用于创建 Itext 实例的 fabric.js 类之一。画布 Itext 是指 Itext 是可移动的，可以根据需要拉伸。在本文中，我们将使用上划线属性。

**方法:**首先导入 fabric.js 库。导入库后，在主体标签中创建一个包含 Itext 的画布块。之后，初始化 Fabric.js 提供的 Canvas 和 Itext 类的一个实例，并使用 overline 属性。

**语法**:

```html
fabric.Itext (Itext , {
    overline : boolean
});
```

**参数:**该函数采用如上所述的单个参数，描述如下:

*   **上划线:**该参数取布尔值。

**示例:**本示例使用 FabricJS 设置画布 Itext 的上划线属性，如下例所示:

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
    <div style="text-align: center;width: 400px;">
        <h1 style="color: green;">
            GeeksforGeeks
        </h1>

        <b>
            Fabric.js | Itext overline Property
        </b>
    </div>

    <div style="text-align: center;">
        <canvas id="canvas" width="400" height="200"
            style="border:1px solid green;">
        </canvas>
    </div>

    <script>
        var canvas = new fabric.Canvas("canvas");

        var geek = new fabric.IText('GeeksforGeeks', {
            overline: true
        });

        console.log(geek.willDrawShadow())
        canvas.add(geek);
        canvas.centerObject(geek);
    </script>
</body>

</html>
```

**输出:**

![](img/8fdc8d8167da48e84e4b0ea76ad33e79.png)