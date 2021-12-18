# p5.js |色相()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-hue-function/](https://www.geeksforgeeks.org/p5-js-hue-function/)

p5.js 中的**色相()函数**用于从颜色或像素数组中提取 HSB 和 HSL 色相值。

**语法:**

```
hue(c)
```

**参数:**该功能接受存储 p5 的单参数 **c** 。颜色对象、颜色组件或 CSS 颜色。

下面的程序说明了 p5.js 中的 hue()函数:

**示例 1:** 本示例使用色相()函数从颜色或像素阵列中提取 HSB 和 HSL 色相值。

```
function setup() {

    // Create Canvas of size 300*80
    createCanvas(300, 80);
}

function draw() {

    // Set background color
    background(220);

    // Initialize color mode to HSB
    colorMode(HSB, 255);

    // Initialize the parameter
    let c = color(0, 126, 100);

    // Sets 'value' to 0
    let value = hue(c); 

    // Set font size
    textSize(16);

    // Set font color
    fill(color('red'));

    // Display result
    text("Hue Value is : " + value, 50, 30);
}
```

**输出:**
![](img/92e28ccd23789de67951527f2c8896eb.png)

**示例 2:** 本示例使用 hue()函数从颜色中提取 HSB 和 HSL 色调值，并将颜色值填充为灰度整数值。

```
function setup() {

    // Create Canvas of size 300*180
    createCanvas(300, 180);
}

function draw() {

    // Set background color
    background(220);

    // Initialize color mode to HSB
    colorMode(HSB, 255);

    // Initialize the parameter
    let c = color(56, 126, 10);

    // Sets 'value' to 56
    let value = hue(c); 

    // Fill the hue value as grayscale
    fill(value);

    // Create rectangle
    rect(50, 15, 35, 70);

    // Display result
    text("Value of Hue is : " + value, 22, 110);
}
```

**输出:**
![](img/2ecfc08e2c468ee9c18551efb701c52f.png)

**参考:**T2】https://p5js.org/reference/#/p5/hue