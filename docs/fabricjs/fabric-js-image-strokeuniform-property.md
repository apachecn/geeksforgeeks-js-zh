# 织物图像纹理均匀性

> 原文:[https://www . geesforgeks . org/fabric-js-image-stroke uniform-property/](https://www.geeksforgeeks.org/fabric-js-image-strokeuniform-property/)

在本文中，我们将看到如何设置统一的笔画宽度图像。画布图像是用于创建图像实例的 fabric.js 类之一。画布图像意味着图像是可移动的，可以根据需要拉伸。strokeUniform 用于锁定统一笔划。

**语法** :

```html
fabric.Image(image, {
strokeUniform : boolean
});
```

**参数**:该功能取单个参数，如上所述，描述如下:

*   **描边均匀**:该参数取布尔值，锁定画布图像的均匀描边。

**示例**:本示例使用 FabricJS 设置画布图像的 strokeUniform 属性，如下例所示:

## 超文本标记语言

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
    <h1 style="color: green;"> 
        GeeksforGeeks 
    </h1> 

    <b> 
        Fabric.js | Image strokeUniform Property 
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
        var canvas = new fabric.Canvas("canvas"); 

        // Getting the image 
        var img = document.getElementById('my-image'); 

        // Creating the image instance 
        var geeks = new fabric.Image(img, {
            stroke:"green",
            strokeUniform : false
        }); 

        canvas.add(geeks); 
        canvas.centerObject(geeks); 
    </script> 
</body> 

</html>
```

**输出:**
![](img/1783c175196f573bd014b43032bc77cf.png)