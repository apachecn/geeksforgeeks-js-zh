# fabric . js Image minimumScaleTrigger 属性

> 原文:[https://www . geeksforgeeks . org/fabric-js-image-minimumsscale trigger-property/](https://www.geeksforgeeks.org/fabric-js-image-minimumscaletrigger-property/)

Fabric.js 是一个用于处理画布的 JavaScript 库。画布图像是用于创建图像实例的 fabric.js 类之一。画布图像意味着图像是可移动的，可以根据需要拉伸。在本文中，我们将使用，minimumScaleTrigger 属性来设置画布图像中的最小比例触发器。

**方法:**首先导入 fabric.js 库。导入库后，在主体标签中创建一个包含图像的画布块。之后，初始化一个由 Fabric 提供的 Canvas 和 image 类的实例。JS 和使用 minimumScaleTrigger 属性用于设置最小比例触发器。之后，在画布上渲染图像。

**语法:**

```
fabric.Image(image, {
    minimumScaleTrigger : number
});
```

**参数:**该函数采用如上所述的单个参数，描述如下:

*   **最小刻度触发器:**该参数取一个数值来指定最小刻度触发器。

**示例:**本示例使用 FabricJS 设置画布图像的 minimumScaleTrigger 属性，如下例所示:

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
        Fabric.js | Image minimumScaleTrigger Property 
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
            minimumScaleTrigger : 1
        }); 

        console.log("minimumScaleTrigger is set to: ",
                    geeks.minimumScaleTrigger)
        canvas.add(geeks); 
        canvas.centerObject(geeks); 
    </script> 
</body> 

</html>
```

![](img/c988d1a6b6210607d100e0dff0c79d70.png)