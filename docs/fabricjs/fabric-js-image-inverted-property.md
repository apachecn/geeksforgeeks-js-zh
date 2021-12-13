# 织物. js 图像反转属性

> 原文:[https://www . geesforgeks . org/fabric-js-image-inverted-property/](https://www.geeksforgeeks.org/fabric-js-image-inverted-property/)

**Fabric.js** 是一个用来处理画布的 JavaScript 库。*画布*图像是用于创建图像实例的**织物. js** 的类别之一。画布图像意味着图像是可移动的，可以根据需要进行拉伸。在本文中，我们将在画布图像中使用*反转*属性。

**逼近**:首先导入 **Fabric.js** 库。导入库后，在主体标签中创建一个包含图像的画布块。之后，初始化一个由 Fabric.js 提供的画布和图像类的实例，并使用*反转的*属性。之后，在画布上渲染图像。

**语法**:

```html
fabric.Image(image, {
    inverted : boolean
});
```

**参数**:该功能取一个参数，如上所述，如下所述。

*   **反转**:该参数取布尔值。

**示例**:本示例使用 **Fabric.js** 设置画布图像的*反转*属性，如下例所示。

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
        Fabric.js | Image inverted Property 
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
            inverted: false
        }); 

        canvas.add(geeks); 
        canvas.centerObject(geeks); 
    </script> 
</body> 

</html>
```

**输出:**

![](img/36075ed8fae58b74c9a5fd59373f01b6.png)