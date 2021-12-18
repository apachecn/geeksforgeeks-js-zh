# p5.js | setGreen()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-setgreen-function/](https://www.geeksforgeeks.org/p5-js-setgreen-function/)

p5.js 中的**设置绿色()功能**用于**在 RGB 颜色模式下设置** *的绿色值。它设置 RGB 格式的第二个值。*

**语法:**

```
setGreen(green)

```

**参数:**该功能接受如上所述的单个参数，描述如下:

*   **绿色:**该参数存储新的绿色值。

下面的程序说明了 p5.js:
**中的 **setGreen()** 函数示例-1:** 本示例使用 **setGreen()** 函数设置 RGB 颜色格式的红色值。

```
/* declare a variable
to store the value of color*/
let backgroundColor;

function setup() {
    /* initialise the variable
    with RGB color format*/
    backgroundColor =
      color(13, 0, 150);
}

function draw() {
    /* Create Canvas of a given size*/

    createCanvas(500, 500);

    // Use of setGreen function
    backgroundColor.setGreen(
      0 + 128 * cos(millis() / 1000));

    /* Pass the initialised variable 
      to background function*/
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
![](img/c44855fffc61ddb586cd74a37ad65421.png)

**示例-2:** 本示例使用 **setGreen()** 函数设置 RGB 颜色格式的红色值。

```
/* declare a variable to 
store the value of color.*/
let backgroundColor;

function setup() {
    /* initialise the variable
    with RGB color format.*/
    backgroundColor = 
      color(0, 0, 0);
}

function draw() {
    // Create Canvas of a given size

    createCanvas(540, 500);

    /* Use of setGreen function
    and initialise it to maximum.*/
    backgroundColor.setGreen(255);

    /* Pass the initialised variable
    to background function.*/
    background(backgroundColor);

    // Set text size
    textSize(30);

    // Set text color
    fill("green");

    // set text
    text("GeeksForGeeks\n ", 135, 125);
    text(
      "A Computer Science Portal For Geeks"
      , 10, 155);

}
```

**输出:**
![](img/0f9115246052356d6bad3c7c6dad65b8.png)

**参考:**T2】https://p5js.org/reference/#/p5.Color/setGreen