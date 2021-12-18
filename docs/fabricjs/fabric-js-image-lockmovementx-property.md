# Fabric.js Image lockMovementX 属性

> 原文:[https://www . geesforgeks . org/fabric-js-image-lock movementx-property/](https://www.geeksforgeeks.org/fabric-js-image-lockmovementx-property/)

**Fabric.js** 是一个用来处理画布的 javascript 库。画布图像是用于创建图像实例的 fabric.js 类之一。画布图像意味着图像是可移动的，可以根据需要拉伸。图像的 lockMovementX 属性用于启用或禁用画布图像的 MovementX。

**方法:**首先导入 fabric.js 库。导入库后，在主体标签中创建一个包含图像的画布块。之后，初始化一个由 Fabric 提供的 Canvas 和 image 类的实例。然后使用 lockMovementX 属性来启用或禁用画布图像的移动。之后，在画布上渲染图像并居中。现在尝试水平移动图像。

**语法:**

```
fabric.Image(image, {
    lockMovementX:Boolean
});

```

**参数:**该函数取两个参数，如上所述，描述如下:

*   **图像:**该参数取图像。
*   **lockMovementX:** 此参数采用布尔值来启用或禁用画布图像的 MovementX。

**示例:**本示例使用 FabricJS 设置画布图像沿 x 轴的左侧位置，如下例所示。

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
    <h1 style="color: green;">GeeksforGeeks</h1> 

    <b>Fabric.js | Image lockMovementX Property </b> 

    <canvas id="canvas" width="400" height="300"
        style="border:2px solid #000000"> 
    </canvas> 

    <img src =
"https://media.geeksforgeeks.org/wp-content/uploads/20200327230544/g4gicon.png"
        width="100" height="100" id="my-image"
        style="display: none;"><br>

    <script> 

        // Create the instance of canvas object
        var canvas = new fabric.Canvas("canvas"); 

        // Getting the image
        var img= document.getElementById('my-image');

        // Creating the image instance 
        var imgInstance = new fabric.Image(img, {
        });

        function lockMovementX(){
            imgInstance = new fabric.Image(img, {
                lockMovementX:true
            });
            canvas.clear();
            canvas.add(imgInstance);
        }
        lockMovementX();

        // Rendering the image to canvas
        canvas.add(imgInstance);
    </script> 
</body> 
</html>
```

**输出:**

![](img/27fc93f71798b5dd49176b0abf07b9e4.png)