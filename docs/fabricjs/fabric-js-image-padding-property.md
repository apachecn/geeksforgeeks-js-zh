# 织物. js 图像填充属性

> 原文:[https://www . geesforgeks . org/fabric-js-image-padding-property/](https://www.geeksforgeeks.org/fabric-js-image-padding-property/)

Fabric.js 是一个用于处理画布的 JavaScript 库。画布图像是用于创建图像实例的 Fabric.js 类之一。Fabric.js 中的图像是可移动的，可以根据需要进行拉伸。在本文中，我们将使用 padding 属性来设置画布图像的填充。

**接近**:首先导入 Fabric.js 库。导入库后，在包含图像的主体标签中创建一个画布块。之后，初始化一个由 Fabric.js 提供的 Canvas 和 Image 类的实例，使用 padding 属性设置 padding，并在 Canvas 上呈现这个 Image。

**语法:**

```html
fabric.Image(image, {
  padding : number
});
```

**参数:**该函数采用如上所述的单个参数，描述如下:

*   **填充**:指定对象和控制边框之间的填充。

**示例**:本示例使用 Fabric.js 设置画布 Image 的填充属性，如下例所示:

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
        Fabric.js | Image padding Property 
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

        // Getting the Image 
        var img = document.getElementById('my-image'); 

        // Creating the Image instance 
        var geeks = new fabric.Image(img, {
            padding:20 
        }); 

        canvas.add(geeks); 
        canvas.centerObject(geeks); 
    </script> 
</body> 
</html>
```

**输出:**

![](img/de3482a7ac9bef7a41b41d8d8105697e.png)