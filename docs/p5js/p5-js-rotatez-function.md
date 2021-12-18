# p5.js | rotateZ()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-rotatez-function/](https://www.geeksforgeeks.org/p5-js-rotatez-function/)

p5.js 中的 **rotateZ()函数**用于围绕 z 轴旋转形状或对象。

**语法:**

```
rotateZ(angle)
```

**参数:**该功能接受单个参数**角度**，该参数存储旋转角度。
下面的程序说明了 p5.js:
**中的 rotateZ()函数示例 1:** 本示例使用 rotateZ()函数来围绕 z 轴旋转对象。

## java 描述语言

```
function setup() {

    // Create Canvas of given size
    createCanvas(580, 550, WEBGL);
}

function draw() {
    // Set the background color
    background(220);

    // Set stroke weight
    strokeWeight(12);

    // Rotation function
    rotate(PI / 7.0);

    // Call to rotateZ function
    rotateZ(millis() / 1000);

    // Draw Rectangle
    rect(3, 3, 200, 39);

    // Draw ellipse
    ellipse(160, 160, 40, 40);
}
```