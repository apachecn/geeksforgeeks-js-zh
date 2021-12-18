# p5.js | red()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-red-function/](https://www.geeksforgeeks.org/p5-js-red-function/)

p5.js 中的 **red()函数**用于从颜色或像素数组中提取红色值。

**语法:**

```
red(c)
```

**参数:**该功能接受存储 p5 的单参数 **c** 。颜色对象、颜色组件或 CSS 颜色。

下面的程序说明了 p5.js 中的 red()函数:

**示例 1:** 本示例使用 red()函数从像素阵列中提取红色值。

```
function setup() {

    // Create Canvas of size 300*80
    createCanvas(300, 80);
}

function draw() {

    // Set background color
    background(220);

    // Initialize the parameter
    let c = color(67, 126, 255, 102);

    // Extract the red value
    let y = red(c);

    // Set the font size
    textSize(16);

    // Set the font color
    fill(color('red'));

    // Display result
    text("Red Value is : " + y, 50, 30);
}
```

**输出:**
![](img/1c237bbf0681835e70d9a5d6db13cd9d.png)

**示例 2:** 本示例使用 red()函数从像素阵列中提取红色值并用作填充颜色。

```
function setup() {

    // Create Canvas of size 300*180
    createCanvas(160, 180);
}

function draw() {

    // Set background color
    background(220);

    // Initialize the parameter
    let c = color(80, 126, 100, 34);

    // Sets 'value' to 80
    let value = red(c); 

    // Fill the color
    fill(value, 0, 0);

    // Create rectangle
    rect(50, 15, 35, 70);

    // Display result
    text("Value of red is : " + value, 22, 110);
}
```

**输出:**
![](img/d6a59f08196354933ca66a2c276933e0.png)

**参考:**T2】https://p5js.org/reference/#/p5/red