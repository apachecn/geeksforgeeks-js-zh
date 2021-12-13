# Fabric.js 图像透明角属性

> 原文:[https://www . geesforgeks . org/fabric-js-image-transparentcorners-property/](https://www.geeksforgeeks.org/fabric-js-image-transparentcorners-property/)

Fabric.js 是一个用于处理画布的 JavaScript 库。画布图像是用于创建图像实例的 fabric.js 类之一。画布图像意味着图像是可移动的，可以根据需要拉伸。透明角落属性用于设置角落是否透明。

**方法:**首先导入 fabric.js 库。导入库后，在主体标签中创建一个包含图像的画布块。之后，初始化一个由 Fabric 提供的 Canvas 和 image 类的实例。JS 并使用 transparentCorners 属性来设置角是否透明。之后，在画布上渲染图像。

**语法:**

```html
fabric.Image(image, {
    transparentCorners : Boolean
});
```

**参数:**该函数采用如上所述的单个参数，描述如下:

*   **透明角落:**该参数取一个布尔值来设置画布图像的透明度。

**示例**:本示例使用 FabricJS 设置画布图像的 transparentCorners 属性，如下例所示:

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
        Fabric.js | Image transparentCorners Property 
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
        var geeks = new fabric.Image(img, { 
        }); 

        function gfg() { 
            geeks = new fabric.Image(img, {  
               transparentCorners: true
            }); 
            canvas.clear(); 

            // Rendering the image to canvas 
            canvas.add(geeks); 

            canvas.centerObject(geeks); 
        } 
        canvas.add(geeks); 
        canvas.centerObject(geeks); 
    </script> 
</body> 

</html>
```

**输出:**

![](img/1f69729b218e5978558e83beb27176a3.png)

**示例:**本示例使用 FabricJS 设置画布图像的 transparentCorners 属性，如下例所示:

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
        Fabric.js | Image transparentCorners Property 
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
        var geeks = new fabric.Image(img, { 
        }); 

        function gfg() { 
            geeks = new fabric.Image(img, {  
               transparentCorners: false
            }); 
            canvas.clear(); 

            // Rendering the image to canvas 
            canvas.add(geeks); 

            canvas.centerObject(geeks); 
        } 
        canvas.add(geeks); 
        canvas.centerObject(geeks); 
    </script> 
</body> 

</html>
```

**输出:**

![](img/9bbdfd71f997979244db9d8a67c59d74.png)