# 织物. js 图像类型属性

> 原文:[https://www . geesforgeks . org/fabric-js-image-type-property/](https://www.geeksforgeeks.org/fabric-js-image-type-property/)

在本文中，我们将看到如何使用 FabricJS 设置画布图像的类型。画布图像意味着图像是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、形状、填充颜色或笔画宽度时，可以自定义图像。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。导入库后，我们将在包含图像的主体标签中创建一个画布块。之后，我们将初始化由 FabricJS 提供的 Canvas 和 Image 的实例，并使用 type 属性设置 Image 的最小比例限制，并在 Canvas 上渲染 Image，如下例所示。

**语法:**

```html
var a = image.type;
```

**示例:**本示例使用 FabricJS 设置画布图像的 type 属性，如下例所示:

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
        Fabric.js | Image type Property 
    </b> 

    <canvas id="canvas" width="400" height="300"
        style="border:2px solid #000000"> 
    </canvas> 

    <img src= 
"https://media.geeksforgeeks.org/wp-content/uploads/20200327230544/g4gicon.png"
        width="100" height="100" id="my-image"
        style="display: none;"> 
    <br> 

    <button onclick="gfg()">Clickme</button> 

    <script> 

        // Creating the instance of canvas object 
        var canvas = new fabric.Canvas("canvas"); 

        // Getting the image 
        var img = document.getElementById('my-image'); 

        // Creating the image instance 
        var imgInstance = new fabric.Image(img, { 
        }); 

        function gfg() { 
            imgInstance = new fabric.Image(img, {  
            }); 
            console.log(imgInstance.type)
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

![](img/4a885e9420e63c12f007124f74f69003.png)