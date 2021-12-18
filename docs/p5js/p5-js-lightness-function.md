# p5.js |明度()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-lightness-function/](https://www.geeksforgeeks.org/p5-js-lightness-function/)

p5.js 中的**明度()函数**用于从颜色或像素阵列中提取 HSL 明度值。

**语法:**

```
lightness(c)
```

**参数:**该功能接受存储 p5 的单参数 **c** 。颜色对象、颜色组件或 CSS 颜色。

下面的程序说明了 p5.js 中的 light()函数:

**示例 1:** 本示例使用明度()函数从像素阵列中提取 HSL 明度值。

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

    // Sets 'value' to 100
    let value = lightness(c); 

    // Set the font size
    textSize(16);

    // Set the font color
    fill(color('red'));

    // Display result
    text("Lightness Value is : " + value, 50, 30);
}
```

**输出:**
![](img/5995991fbd0f8c96b67e12986a119128.png)

**示例 2:** 本示例使用明度()函数从像素阵列中提取 HSL 明度值，并将其用作灰度值。

```
function setup() {

    // Create Canvas of size 300*80
    createCanvas(300, 180);
}

function draw() {

    // SEt background color
    background(220);

    // Initialize color mode to HSB
    colorMode(HSL, 255);

    // Initialize the parameter
    let c = color(56, 126, 10);

    // Sets 'value' to 10
    let value = lightness(c); 

    // Fill the color value
    fill(value);

    // Create rectangle
    rect(50, 15, 35, 70);

    // Display result
    text("Value of Lightness is : " + value, 22, 110);
}
```

**输出:**
![](img/8c4d98cb4bee80ad54107296f99467b7.png)

**参考:**T2】https://p5js.org/reference/#/p5/lightness