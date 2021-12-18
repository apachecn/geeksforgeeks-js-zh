# 织物. js 图像角样式属性

> 原文:[https://www . geesforgeks . org/fabric-js-image-corner style-property/](https://www.geeksforgeeks.org/fabric-js-image-cornerstyle-property/)

**Fabric.js** 是一个用来处理画布的 javascript 库。画布图像是用于创建图像实例的 fabric.js 类之一。画布图像意味着图像是可移动的，可以根据需要拉伸。图像的 cornerStyle 属性用于更改样式，即画布图像控制角的形状。

**方法:**首先导入 fabric.js 库。导入库后，在主体标签中创建一个包含图像的画布块。之后，初始化一个由 Fabric 提供的 Canvas 和 image 类的实例。JS 并使用图像对象的 cornerStyle 属性更改画布图像的控制角的样式。

**语法:**

```
fabric.Image(image, {
    cornerStyle:string
});
```

**参数:**该函数取两个参数，如上所述，描述如下:

*   **图像:**该参数取图像。
*   **角样式:**此参数定义画布图像的控制角的样式，即矩形或圆形。

**示例:**本示例使用 FabricJS 更改画布图像的控制角的样式，如下例所示。

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
    <h1 style="color: green;">GeeksforGeeks</h1> 
    <b>Fabric.js | Image cornerStyle Property </b> 

    <canvas id="canvas" width="400" height="300"
        style="border:2px solid #000000"> 
    </canvas> 

    <img src =
"https://media.geeksforgeeks.org/wp-content/uploads/20200327230544/g4gicon.png" 
        width="100" height="100" id="my-image"
        style="display: none;">

    <script> 

        // Create the instance of canvas object
        var canvas = new fabric.Canvas("canvas"); 

        // Getting the image
        var img= document.getElementById('my-image');

        // Creating the image instance 
        var imgInstance = new fabric.Image(img, {
            cornerColor:"red",

          // Setting the corner style to circle
            cornerStyle:"circle"
        });

        // Rendering the image to canvas
        canvas.add(imgInstance);
    </script> 
</body> 

</html>
```

**输出:**

![](img/0a0115c8991eaf56fcc6287451a11bae.png)