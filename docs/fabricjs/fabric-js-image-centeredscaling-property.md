# 织物图像中心缩放属性

> 原文:[https://www . geesforgeks . org/fabric-js-image-centered scaling-property/](https://www.geeksforgeeks.org/fabric-js-image-centeredscaling-property/)

Fabric.js 是一个用于处理画布的 JavaScript 库。画布图像是用于创建图像实例的 Fabric.js 类之一。Fabric.js 中的图像是可移动的，可以根据需要进行拉伸。在本文中，我们将使用中心缩放属性来启用画布图像中的中心缩放。

**接近**:首先导入 Fabric.js 库。导入库后，在包含图像的主体标签中创建一个画布块。之后，初始化 Fabric.js 提供的 canvas 和 Image 类的一个实例，设置 centeredScaling 属性以启用居中缩放并在 Canvas 上呈现图像。

**语法**:

```html
fabric.Image(image, {
  centeredScaling: boolean
});
```

**参数**:该功能接受如上所述的单个参数，描述如下:

*   **居中缩放**:此参数定义是启用还是禁用居中缩放。

**示例**:本示例使用 Fabric.js 设置画布图像的中心缩放属性，如下例所示:

## 超文本标记语言

```html
<html>
<head> 
    <!-- Adding the FabricJS library -->
    <script src= 
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js"> 
    </script> 
</head> 
<body> 
    <h1 style="color: green;"> 
        GeeksforGeeks 
    </h1> 
    <b> 
        Fabric.js | Image centeredScaling Property 
    </b> 
    <canvas id="canvas" width="400" height="300"
            style="border:2px solid #000000"> 
    </canvas> 
    <img src= 
"https://media.geeksforgeeks.org/wp-content/uploads/20200327230544/g4gicon.png"
        width="100" height="100" id="my-image"
        style="display: none;"> 
    <br>
    <script> 
        // Creating the instance of canvas object 
        var canvas =
            new fabric.Canvas("canvas"); 

        // Getting the image 
        var img =
            document.getElementById('my-image'); 

        // Creating the image instance 
        var geeks = new fabric.Image(img, {
            centeredScaling : true
        }); 

        canvas.add(geeks); 
        canvas.centerObject(geeks); 
    </script> 
</body> 
</html>
```

**输出:**

![](img/6f4c2a5c6509a07804ef84220e92073c.png)