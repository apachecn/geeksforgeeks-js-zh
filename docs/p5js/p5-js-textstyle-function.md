# p5.js | textStyle()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-textstyle-function/](https://www.geeksforgeeks.org/p5-js-textstyle-function/)

p5.js 中的 **textStyle()功能**用于将系统字体的文本样式设置或返回到 NORMAL、ITALIC、BOLD 或 BOLDITALIC。这可能会被 CSS 样式覆盖。

**语法:**

```
textStyle(style)
```

或者

```
textStyle()
```

**参数:**该功能接受单参数**样式**，存储样式常量。

下面的程序说明了 p5.js 中的 textStyle()函数:

**示例 1:** 本示例使用 textStyle()函数设置文本的样式。

```
function setup() {

    // Create Canvas of given size
    createCanvas(380, 170);
}

function draw() {

    let string = "GeeksforGeeks";

    // Set the background color
    background(220);

    // Set the text style
    textStyle(ITALIC);

    // Set the text size
    textSize(16);

    // Set the text 
    text(string, 20, 30);

    // Set text styling
    textStyle(BOLD);

    text(string, 20, 70);

    // Set text styling
    textStyle(BOLDITALIC);

    text(string, 20, 110);
}
```

**输出:**
![](img/229e0872418cfac55098d2ff48c15bdb.png)

**示例 2:** 本示例使用 textStyle()函数返回文本的样式。

```
function setup() {

    // Create Canvas of given size
    createCanvas(380, 170);
}

function draw() {

    let string = "GeeksforGeeks";

    // Set the background color
    background(220);

    // Set text style
    textStyle(BOLD);

    // Set the text size
    textSize(16);

    // Get the value of text style
    var u = textStyle();

    // Set the stroke color
    stroke(255, 204, 0);

    // Display the result
    text("Value of Text Style is : " + u, 50, 30);
}
```

**输出:**
![](img/7084278be0691f3414430139c1ee6a0e.png)

**参考:**T2】https://p5js.org/reference/#/p5/textStyle