# 如何使用 p5.js 设计平面着色图形？

> 原文:[https://www . geesforgeks . org/how-design-flat-shading-graphics-using-P5-js/](https://www.geeksforgeeks.org/how-to-design-flat-shading-graphics-using-p5-js/)

平面阴影是三维计算机图形学中使用的一种照明技术，它根据多边形表面法线和光源方向之间的角度、它们各自的颜色以及光源的强度来给物体的每个多边形着色。

*   对多边形的每个面计算一次颜色。
*   多边形中的所有像素都设置为相同的颜色
*   适用于平面物体。

**示例:**

## java 描述语言

```
// Store the angle value in a variable
var angle = 0.1;

// Set the canvas size
function setup() {
    createCanvas(500, 500, WEBGL);
}

// Function to draw the Flat 
// Shading Graphics
function draw() {

    // Create a directional light with 
    // specified color and direction
    directionalLight(25, 250, 50, 101, 0, 0);

    // Set the background color
    background(50, 50, 200);

    // Set the rotation angle
    rotateX(angle);
    rotateY(angle * 0.3);
    rotateZ(angle * 1.2);

    // Set the fill color
    fill(0, 0, 205);

    noStroke();
    ambientMaterial(300);
    cone(100);
    angle += 0.03;
}
```

**输出:**

<video class="wp-video-shortcode" id="video-539300-1" width="640" height="360" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20201230163331/flat-shading-vdo.mp4?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/20201230163331/flat-shading-vdo.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20201230163331/flat-shading-vdo.mp4)</video>