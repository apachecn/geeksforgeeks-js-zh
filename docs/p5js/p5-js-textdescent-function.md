# P5 . js | TextDression()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-textdescent-function/](https://www.geeksforgeeks.org/p5-js-textdescent-function/)

p5.js 中的**TextDression()函数**用于找出当前字体在其当前大小下的下降。下降可以定义为基线以下最长下降字符的距离，以像素为单位。

**语法:**

```
textDescent()
```

**参数:**此功能无参数。

**返回值:**返回一个数字，以像素为单位表示下降。

下面的例子说明了 p5.js 中的**TextDression()函数**:

**示例 1:** 本示例显示了使用默认字体的文本下降。

```
let inputElem;
let currfontSize = 28;
let fontBaseline = 150;

function setup() {
  createCanvas(600, 300);

  // Create button to increase font size
  let fontBtn = createButton("Increase Font Size");
  fontBtn.mouseClicked(() => {
    currfontSize += 1;
  });
  fontBtn.position(20, 70);

  // Create input box
  inputElem = createInput("");
  inputElem.position(20, 40);
}

function draw() {
  clear();
  textSize(18);
  text("Write in input to change the text and observe text descent", 10, 20);
  textSize(currfontSize);

  // This value depends on the font used
  let fontScalar = 0.8;

  // Display text and line if input not empty
  let enteredText = inputElem.value();
  if (enteredText != "") {
    text(enteredText, 20, fontBaseline);

    // Draw the Base line
    stroke("black");
    line(0, fontBaseline, width, fontBaseline);

    // Draw the Descent Line
    stroke("green");
    descVal = textDescent() * fontScalar;
    line(0, fontBaseline + descVal, width, fontBaseline + descVal);
    noStroke();

    textSize(18);
    text("Text Descent Value: " + descVal, 20, 275);
  }
}
```

**输出:**

![textDescent-defaultFont](img/698d86fcfb8c35e76884c671e5b8d9d1.png)

**示例 2:** 本示例显示了使用自定义字体的文本下降。

```
let inputElem;
let currfontSize = 28;
let fontBaseline = 150;
let newFont;

function preload() {
  newFont = loadFont("fonts/Montserrat.otf");
}

function setup() {
  createCanvas(600, 300);

  textFont(newFont);

  // Create button to increase font size
  let fontBtn = createButton("Increase Font Size");
  fontBtn.mouseClicked(() => {
    currfontSize += 1;
  });
  fontBtn.position(20, 70);

  // Create input box
  inputElem = createInput("");
  inputElem.position(20, 40);
}

function draw() {
  clear();
  textSize(18);
  text("Write in input to change the text and observe text descent", 10, 20);
  textSize(currfontSize);

  // This value depends on the font used
  let fontScalar = 0.8;

  // Display text and line if input not empty
  let enteredText = inputElem.value();
  if (enteredText != "") {
    text(enteredText, 20, fontBaseline);

    // Sraw the Base line
    stroke("black");
    line(0, fontBaseline, width, fontBaseline);

    // Draw the Descent Line
    stroke("green");
    descVal = textDescent() * fontScalar;
    line(0, fontBaseline + descVal, width, fontBaseline + descVal);
    noStroke();

    textSize(18);
    text("Text Descent Value: " + descVal, 20, 275);
  }
}
```

**输出:**

![textDescent-loadedFont](img/cb4a3e92dcd84f712997279b9467e0b2.png)

**在线编辑:**[https://editor.p5js.org/](https://editor.p5js.org/)

**环境设置:**

**参考:**T2】https://p5js.org/reference/#/p5/textDescent