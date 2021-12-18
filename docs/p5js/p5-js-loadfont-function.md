# p5.js | loadFont()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-loadfont-function/](https://www.geeksforgeeks.org/p5-js-loadfont-function/)

**loadFont()** 函数用于从文件或网址加载字体，并将其作为 PFont 对象返回。加载的字体是一个 opentype 字体文件，格式为**。otf** 或**。ttf** 。
此方法本质上是异步的，因此在使用字体之前可能不会结束。因此建议在**预加载()功能**中加载字体。字体最好从相对路径加载，因为由于浏览器的安全特性，某些浏览器可能会阻止从其他远程位置加载。
**语法:**

```
loadFont(path, callback, onError)
```

**参数:**该功能接受三个参数，如上所述，描述如下:

*   **路径:**是必须加载字体的路径。它可以是一个
*   **回调:**这是加载字体后的函数，是可选参数。
*   **onError:** 这是一个函数，如果字体由于任何错误而没有加载，就会调用这个函数，它是一个可选参数。

**返回值:**返回 **p5。字体**给定字体的对象。
以下示例说明了 p5.js:
**示例 1:**
中的 **loadFont()** 功能

## java 描述语言

```
let newFont;

// Loading font
function preload() {
  newFont =
    loadFont('fonts/Montserrat.otf');
}

//  Canvas area and color
function setup() {
  createCanvas(400, 200);
  textSize(20);
  fill("red");
  text('Click once to write using '
        + 'a new font', 20, 20);
  fill("black");

  text('Using the default font', 20, 60);
  text('This is text written using'
        + ' the new font', 20, 80);
}

// Changing font
function mouseClicked() {
  textFont(newFont);
  textSize(20);
  text('Using the Montserrat font',
                        20, 140);

  text('This is text written using'
        + ' the new font', 20, 160);
}
```