# 织物. js 图像宽度属性

> 原文:[https://www . geesforgeks . org/fabric-js-image-width-property/](https://www.geeksforgeeks.org/fabric-js-image-width-property/)

Fabric.js 是一个用于处理画布的 JavaScript 库。画布图像是用于创建图像实例的 fabric.js 类之一。画布图像意味着图像是可移动的，可以根据需要拉伸。图像的**宽度属性**用于设置图像的宽度。

**方法:**首先导入 fabric.js 库。导入库后，在主体标签中创建一个包含图像的画布块。之后，初始化一个由 Fabric 提供的 Canvas 和 image 类的实例。JS 并使用 width 属性设置画布图像的高度。之后，在画布上渲染图像。

**语法:**

```
fabric.Image(image, {
    width: Number
});
```

**参数:**该函数采用如上所述的单个参数，描述如下:

*   **宽度:**该参数取一个数字来设置画布图像的宽度。

**示例:**本示例使用 FabricJS 设置画布图像的宽度，如下例所示:

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
        Fabric.js | Image visible Property 
    </b> 

    <canvas id="canvas" width="400" height="300"
        style="border:2px solid #000000"> 
    </canvas> 

    <img src= 
"https://media.geeksforgeeks.org/wp-content/uploads/20200327230544/g4gicon.png"
        width="100" height="100" id="my-image"
        style="display: none;"> 
    <br> 

    <button onclick="wid()">Clickme</button> 

    <script> 

        // Creating the instance of canvas object 
        var canvas = new fabric.Canvas("canvas"); 

        // Getting the image 
        var img = document.getElementById('my-image'); 

        // Creating the image instance 
        var imgInstance = new fabric.Image(img, { 
        }); 

        function wid() { 
            imgInstance = new fabric.Image(img, {  
                width: 250
            }); 
            canvas.clear(); 

            // Rendering the image to canvas 
            canvas.add(imgInstance); 

            canvas.centerObject(imgInstance); 
        } 
        canvas.add(imgInstance); 
        canvas.centerObject(imgInstance); 
    </script> 
</body> 

</html>
```

**输出:**

*   **点击按钮前:**

![](img/61d8f14bacd1851996552a07da2468ff.png)

*   **点击按钮后:**

![](img/0be4ebbc604bf8d33256c172931bbca0.png)