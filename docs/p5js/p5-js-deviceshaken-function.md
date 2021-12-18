# P5 . js device shaked()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-deviceshaken-function/](https://www.geeksforgeeks.org/p5-js-deviceshaken-function/)

当设备总加速度变化加速度 x 和加速度 y 值大于阈值时，调用函数**deviceshanded()**函数。

默认阈值设置为 30，可以使用 **setShakeThreshold()** 功能进行更改。

它可以用作移动设备中的传感器，如检测运动、加速度、旋转、航向和位置。

**语法:**

```
deviceShaken()
```

现在我们将在安卓手机上运行一些例子。

**第一步:**使用任意浏览器“https://editor.p5js.org/”在手机上打开 p5.js 的在线网页编辑器

**第二步:**在编辑器部分写下下面的代码，运行它查看输出。

**例 1:**

## java 描述语言

```
// Set the variable as 0
var value = 0;

// Set the function
function setup() {
    createCanvas(windowWidth, windowHeight);

    // Set the background as value which
    // will be dynamic
    background(value);
}

// Set the draw function
function draw() {

    // Set the properties of text
    background(value);
    fill(0, 0, 255);
    textAlign(CENTER, CENTER);
    textSize(25);

    // Set the limit for value
    value = constrain(value - 2, 0, 200)

    // If the value is greater than 10
    if (value > 10) {
        text("Shaking Device", width / 2, height / 2);
    } else {
        text("Device is Silent ", width / 2, height / 2);
    }
}

function deviceShaken() {

    // Now increase the value.
    value = constrain(value + 5, 0, 255)
}
```

**输出:**当我们摇动设备时，我们将获得输出

![](img/fb1d0c28ad637f5f88056cdb73e08d8d.png)

**例 2:**

## java 描述语言

```
// Set value to zero
let value = 0;

// Set the draw function
function draw() {

    // When the device is moved
    // in the all direction then
    // the colour fill filled
    fill(value);

    // Set the shape of thr Graphics
     rect(50, 50, 100, 100);
}

// Apply the deviceShaken function
function deviceShaken() {

    // Increment the value everytime by 10
    value = value + 10;

    // If the value become greater than 255
    // then reset the value to zero.
    if (value > 255) {
        value = 0;
    }
}
```

**输出:**

![](img/d3b34586d6f5d1e0f5fe435f05b2cb3a.png)

**参考:**T2https://p5js.org/reference/#/p5/deviceShaken