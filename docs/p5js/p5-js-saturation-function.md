# p5.js |饱和度()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-saturation-function/](https://www.geeksforgeeks.org/p5-js-saturation-function/)

p5.js 中的**饱和度()函数**用于从颜色或像素阵列中提取 HSL 和 HSB 饱和度值。

**语法:**

```
saturation(c)
```

**参数:**该功能接受存储 p5 的单参数 **c** 。颜色对象、颜色组件或 CSS 颜色。

下面的程序说明了 p5.js 中的饱和度()函数:

**示例 1:** 本示例使用饱和度()函数从像素阵列中提取 HSL 和 HSB 饱和度值。

```
function setup() {

    // Create Canvas of size 300*80
    createCanvas(300, 80);
}

function draw() {

    // Set background color
    background(220);

    // Initialize color mode to HSB
    colorMode(HSL, 255);

    // Initialize the parameter
    let c = color(0, 126, 100);

    // Sets 'value' to 126
    let value = saturation(c); 

    // Set the font size
    textSize(16);

    // Set the font color
    fill(color('red'));

    // Display result
    text("Saturation Value is : "
            + int(value), 50, 30);
}
```

**输出:**
![](img/526090dfdee67c3eed9ef584ef8eaaa5.png)

**示例 2:** 本示例使用饱和度()函数从像素阵列中提取 HSL 和 HSB 饱和度值，并将其填充为灰度值。

```
function setup() {

    // Create Canvas of size 300*180
    createCanvas(300, 180);
}

function draw() {

    // Set the background color
    background(220);

    // Initialize color mode to HSB
    colorMode(HSB, 255);

    // Initialize the parameter
    let c = color(56, 126, 10);

    // Sets 'value' to 126
    let value = saturation(c); 

    // Fill the color
    fill(value);

    // Create rectangle
    rect(50, 15, 35, 70);

    // Display result
    text("Value of Saturation is : "
            + int(value), 22, 110);
}
```

**输出:**
![](img/2246e2b1cc208483472fd9f381012ecd.png)

**参考:**T2】https://p5js.org/reference/#/p5/saturation