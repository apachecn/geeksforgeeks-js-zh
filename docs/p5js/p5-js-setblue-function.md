# p5.js | setBlue()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-setblue-function/](https://www.geeksforgeeks.org/p5-js-setblue-function/)

p5.js 中的**设置蓝色()功能**用于**在 RGB 颜色模式下设置** *的蓝色值。它设置 RGB 格式的第三个值。*

**语法:**

```
setBlue(blue)

```

**参数:**该功能接受如上所述的单个参数，描述如下:

*   **蓝色:**该参数存储新的蓝色值。

下面的程序举例说明了 p5.js:
**中的 **setBlue()** 功能示例-1:** 本示例使用 **setBlue()** 功能设置 RGB 颜色格式的红色值。

```
/* declare a variable to 
store the value of color*/
let backgroundColor;

function setup() {
    /* initialise the variable
    with RGB color format*/
    backgroundColor = color(13, 40, 0);
}

function draw() {
    // Create Canvas of a given size

    createCanvas(500, 500);

    // Use of setBlue function
    backgroundColor.setBlue(
      0 + 128 * cos(millis() / 1000));

    /* Pass the initialised 
    variable to background function*/
    background(backgroundColor);

    // Set text size
    textSize(30);

    // Set text color
    fill("white");

    // set text
    text("GeeksForGeeks", 125, 125);

}
```

**输出:**
![](img/ada3326a31507ffe4eb0fefc38f10382.png)

**示例 2:** 本示例使用 **setBlue()** 功能设置 RGB 颜色格式的红色值。

```
/* declare a variable
to store the value of color*/
let backgroundColor;

function setup() {
    /* initialise the variable
    with RGB color format*/
    backgroundColor = color(0, 0, 0);
}

function draw() {
    // Create Canvas of a given size

    createCanvas(540, 500);

    /* Use of setBlue function
    and initialise it to maximum*/
    backgroundColor.setBlue(255);

    /* Pass the initialised 
    variable to background function*/
    background(backgroundColor);

    // Set text size
    textSize(30);

    // Set text color
    fill("white");

    // set text
    text("GeeksForGeeks\n ", 135, 125);
    text(
      "A Computer Science Portal For Geeks"
      , 10, 155);

}
```

**输出:**
![](img/00bb541f6a4e9ae756bd3f92d1546fec.png)

**参考:**T2】https://p5js.org/reference/#/p5.Color/setBlue