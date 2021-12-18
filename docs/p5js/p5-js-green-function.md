# p5.js |绿色()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-green-function/](https://www.geeksforgeeks.org/p5-js-green-function/)

p5.js 中的**绿色()函数**用于从颜色或像素阵列中提取绿色值。

**语法:**

```
green(c)
```

**参数:**该功能接受存储 p5 的单参数 **c** 。颜色对象、颜色组件或 CSS 颜色。

下面的程序说明了 p5.js 中的 green()函数:

**示例 1:** 本示例使用 green()函数从颜色或像素阵列中提取绿色值。

```
function setup() {

    // Create Canvas of size 300*80
    createCanvas(300, 80);
}

function draw() {

    // Set background color
    background(220);

    // Initialize the parameter
    let c = color(0, 126, 255, 102);

    // Extract the green value
    let y = green(c);

    // Set font size
    textSize(16);

    // Set font color
    fill(color('red'));

    // Display result
    text("Green Value is : " + y, 50, 30);
} 
```

**输出:**
![](img/4a3c9fc7f1121744459736a5ea7b4637.png)

**示例 2:** 本示例使用 green()函数提取绿色值并填充到矩形中。

```
function setup() {

    // Create Canvas of size 300*80
    createCanvas(160, 180);
}

function draw() {

    // Set the background color
    background(220);

    // Initialize the parameter
    let c = color(0, 126, 100, 34);

    // Sets 'value' to 126
    let value = green(c); 

    // Fill the color
    fill(0, value, 0);

    // Create rectangle
    rect(50, 15, 35, 70);

    // Display result
    text("Value of green is : " + value, 22, 110);
}
```

**输出:**
![](img/98fa10c8c0a1a72c30b6f6207b7e533e.png)
**参考:**[https://p5js.org/reference/#/p5/green](https://p5js.org/reference/#/p5/green)