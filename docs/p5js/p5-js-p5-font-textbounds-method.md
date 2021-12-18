# p5.js | p5。字体文本边界()方法

> 原文:[https://www . geesforgeks . org/P5-js-P5-font-textbounds-method/](https://www.geeksforgeeks.org/p5-js-p5-font-textbounds-method/)

p5 的 **textBounds()方法**。p5.js 中的字体是使用给定字符串所使用的字体为其返回一个紧密的边界框。此方法仅支持单行。
**语法:**

```
textBounds( line, x, y, [fontSize], [options] )

```

**参数:**该功能接受上述五个参数，描述如下:

*   **行:**它是一个字符串，表示必须为其找到边界框的文本行。
*   **x:** 是表示 x 位置的数字。
*   **y:** 是表示 y 位置的数字。
*   **字体大小:**这是一个数字，表示要使用的字体大小。默认值为 12。这是一个可选参数。
*   **选项:**是一个可以用来指定 opentype 选项的对象。Opentype 字体包含对齐和基线选项等选项。默认值为“左”和“字母”。这是一个可选参数。

以下示例说明了 p5.js 中的 **textBounds()函数**:
**示例 1:**

## java 描述语言

```
let inputElem;
let currFont;

function preload() {
  currFont = loadFont("fonts/Montserrat.otf");
}

function setup() {
  createCanvas(600, 300);

  textFont(currFont);
}

function draw() {
  clear();
  textSize(16);
  let text1 = "Hello GeeksforGeeks";
  let text2 = "GeeksforGeeks is a computer science portal";
  text("Below is the example of text bounds using 2 font sizes", 20, 20);

  // Set new font size
  let fontSizeSmall = 16;
  textSize(fontSizeSmall);
  // Get the bounding box dimensions
  let bounding_box = currFont.textBounds(text1, 20, 50, fontSizeSmall);
  // Draw the bounding box
  fill(255);
  stroke(0);
  rect(bounding_box.x, bounding_box.y, bounding_box.w, bounding_box.h);
  fill(0);
  noStroke();
  // Show the text
  text(text1, 20, 50);

  // Set new font size
  let fontSizeLarge = 22;
  textSize(fontSizeLarge);
  // Get the bounding box dimensions
  let bounding_box2 = currFont.textBounds(text2, 20, 100, fontSizeLarge);
  // Draw the bounding box
  fill(255);
  stroke(0);
  rect(bounding_box2.x, bounding_box2.y, bounding_box2.w, bounding_box2.h);
  fill(0);
  noStroke();

  text(text2, 20, 100);
}
```