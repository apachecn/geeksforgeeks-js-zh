# p5.js | setRed()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-setred-function/](https://www.geeksforgeeks.org/p5-js-setred-function/)

p5.js 中的**设置红色()功能**用于**在 RGB 颜色模式下设置** *的红色值。它设置 RGB 格式的第一个值。*

**语法:**

```
setRed(red)

```

**参数:**该功能接受如上所述的单个参数，描述如下:

*   **红色:**该参数存储新的红色值。

下面的程序说明了 p5.js:
**中的 **setRed()** 功能示例- 1:** 本示例使用 **setRed()** 功能设置 RGB 颜色格式的红色值。

```
/* declare a variable to 
 store the value of color*/
let backgroundColor;

function setup() {
    /* initialise the variable
     with RGB color format*/
    backgroundColor = color(0, 50, 150);
}

function draw() {
    // Create Canvas of a given size

    createCanvas(500, 500);

    // Use of setRed function
    backgroundColor.setRed(
      0 + 128 * cos(millis() / 1000));

    /* Pass the initialized 
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
![](img/a974a3506b9e022bf8deda0b8e4b6293.png)

**示例-2:** 本示例使用 **setRed()** 功能设置 RGB 颜色格式的红色值。

```
/* declare a variable to
store the value of color*/
let backgroundColor;

function setup() {
    /* initialise the variable
    with RGB color format*/
    backgroundColor = color(0, 0, 0);
}

function draw() {
    // Create Canvas of a given size

    createCanvas(540, 500);

    /* Use of setRed function 
    and initialise it to maximum*/
    backgroundColor.setRed(255);

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
      "A Computer Science Portal For Geeks",
      10, 155);

}
```

**输出:**
![](img/9e02622951d7c1e6e6d1966a07c7c6e1.png)

**参考:**T2】https://p5js.org/reference/#/p5.Color/setRed