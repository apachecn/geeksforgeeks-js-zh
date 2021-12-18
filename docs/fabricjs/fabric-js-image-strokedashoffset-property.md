# fabric . js Image strokeDashOffset 属性

> 原文:[https://www . geesforgeks . org/fabric-js-image-strokedashoffset-property/](https://www.geeksforgeeks.org/fabric-js-image-strokedashoffset-property/)

**Fabric.js** 是一个用来处理**画布**的 JavaScript 库。画布图像是用于创建图像实例的 fabric.js 类之一。画布图像意味着图像是可移动的，可以根据需要拉伸。**笔画偏移**属性用于设置画布图像的笔画偏移

**接近**:首先导入 fabric.js 库。导入库后，在主体标签中创建一个包含图像的画布块。之后，初始化一个由 Fabric 提供的 Canvas 和 image 类的实例。使用**笔画偏移**属性设置画布图像的笔画偏移。之后，在画布上渲染图像。

**语法**:

```
fabric.Image(image, {
strokeDashOffset : number
});
```

**参数**:该功能取单个参数，如上所述，描述如下:

*   **描边偏移**:该参数取一个数值来设置画布图像的描边偏移。

**示例**:本示例使用 FabricJS 设置画布图像的 strokeDashOffset 属性，如下例所示:

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
    <h1 style="color: green;"> 
      GeeksforGeeks 
    </h1> 

    <b> 
      Fabric.js Image strokeDashOffset Property 
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
        strokeMiterLimit : 100,
        strokeDashOffset :10,
        strokeDashArray: [10], 
        strokeWidth:3
      }); 

      canvas.add(geeks); 
      canvas.centerObject(geeks); 
    </script> 
  </body> 

</html>
```

**输出:**

![](img/05b1fe34b73ea573d9ede50d9fc719f9.png)