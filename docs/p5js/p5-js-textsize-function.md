# p5.js | textSize()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-textsize-function/](https://www.geeksforgeeks.org/p5-js-textsize-function/)

p5.js 中的 **textSize()功能**用于设置或返回文本的字体大小。该函数用于对 text()函数的所有后续调用。

**语法:**

```
textSize(size)
```

或者

```
textSize()
```

**参数:**该功能接受单参数**大小**，以像素为单位存储文本的大小。

下面的程序说明了 p5.js 中的 textSize()函数:

**示例 1:** 本示例使用 textSize()函数设置文本的字体大小。

```
function setup() {

    // Create Canvas of given size
    createCanvas(380, 170);
}

function draw() {

    let string = "GeeksforGeeks";

    // Set the background color
    background(220);

    // Set the text size
    textSize(30);

    // Set the text 
    text(string, 100, 30);
}
```

**输出:**
![](img/7b1b05cdfce9976c9cd4863e1ddfe68e.png)

**示例 2:** 本示例使用 textSize()函数返回文本的字体大小。

```
function setup() {

    // Create Canvas of given size
    createCanvas(380, 170);
}

function draw() {

    let string = "GeeksforGeeks";

    // Set the background color
    background(220);

    // Set the text size
    textSize(16);

    // store the size of text
    var u = textSize();

    // Set the stroke color
    stroke(255, 204, 0);

    // Display result
    text("Value of Text Size is : "
            + u, 50, 30);
}
```

**输出:**
![](img/31c2a1bcf2394cf06a4955d1ab981189.png)

**参考:**T2】https://p5js.org/reference/#/p5/textSize