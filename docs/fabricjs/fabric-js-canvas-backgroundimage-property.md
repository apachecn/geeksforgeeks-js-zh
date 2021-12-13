# fabric . js Canvas background image 属性

> 原文:[https://www . geesforgeks . org/fabric-js-canvas-background image-property/](https://www.geeksforgeeks.org/fabric-js-canvas-backgroundimage-property/)

在本文中，我们将看到如何使用 *backgroundImage* 属性在 **Fabric.js** 中设置**画布**的背景图像。****fabric . js**中的画布用作 HTML 提供的原生画布对象的包装器。它提供了对底层画布的高级访问，允许它有一个对象模型，允许解析 SVG 文件，并允许以直观的方式与画布交互。**

****方法:**为了实现这一点，我们将使用一个名为 **Fabric.js** 的 JavaScript 库。导入库后，我们将在 body 标签中创建画布块。之后，我们将初始化由 **Fabric.js** 提供的画布对象的一个实例，并使用 *backgroundImage* 属性更改画布的背景图像。**

****语法:****

```html
fabric.Canvas(canvasElement, {
    backgroundImage: String | Fabric.Image
});
```

****参数:**该属性接受一个参数，如上所述，如下所述。**

*   ****backgroundImage:** 它是包含图像网址或结构的字符串。指定画布背景图像的图像对象。**

**下面的例子说明了在 JavaScript 中使用 fabric . js Canvas*background image*属性。**

****示例 1:** 本示例使用字符串 URL 来更改画布的背景图像。**

## **超文本标记语言**

```html
<!DOCTYPE html>
<html>

<head>
    <!-- Adding the FabricJS library -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <div style="text-align:center;width:500px;">
        <h1 style="color:green;">
            GeeksforGeeks
        </h1>
        <b>
            Fabric.js | Canvas backgroundImage Property
        </b>
    </div>

    <canvas id="canvas" width="660" height="250" 
        style="border:1px solid #000000">
    </canvas>

    <script>

        // Initiate a Canvas instance 
        let canvas = new fabric.Canvas("canvas", {

            // Set the background image 
            // of the Canvas
            backgroundImage:
"https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-logo.png"
        });
    </script>
</body>

</html>
```

****输出:****

**![](img/8ffd01e29f1ea6bc7b4c1bfba7cc6690.png)**

****示例 2:** 本示例使用了一个织物。对象来更改画布的背景图像。**

## **超文本标记语言**

```html
<!DOCTYPE html>
<html>

<head>
    <!-- Adding the FabricJS library -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <div style="text-align: center;
              width:660px;">
        <h1 style="color:green;">
            GeeksforGeeks
        </h1>
        <b>
            Fabric.js | Canvas backgroundImage Property
        </b>
    </div>

    <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-logo.png"
        id="my_img" style="display:none">

    <canvas id="canvas" width="660" height="250" 
        style="border:1px solid #000000">
    </canvas>

    <script>

        // Select the image from the document
        let selectedImage =
            document.querySelector("#my_img");

        // Create a Fabric.Image object
        let bg_img = new fabric.Image(selectedImage);

        // Initiate a Canvas instance 
        let canvas = new fabric.Canvas("canvas", {

            // Set the background image
            // of the Canvas to the above
            // Fabric.Image object
            backgroundImage: bg_img
        });
    </script>
</body>

</html>
```

****输出:****

**![](img/8ffd01e29f1ea6bc7b4c1bfba7cc6690.png)**