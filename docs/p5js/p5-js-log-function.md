# p5.js | log()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-log-function/](https://www.geeksforgeeks.org/p5-js-log-function/)

p5.js 中的 **log()函数**用于获取 log()函数参数输入的任意数字的自然对数(以“e”为底)。

**语法:**

```
log(x)
```

**参数:**该函数接受单个参数 **x** ，该参数为大于零(0)的任意数字，作为将要计算其自然对数的输入。

**返回值:**返回大于零(0)的任意输入数的自然对数。

下面的程序说明了 p5.js 中的 log()函数:

**示例:**本示例使用 log()函数获取任意输入数字的自然对数值。

## java 描述语言

```
function setup() {

    // Create Canvas of size 270*80
    createCanvas(550, 130);
}

function draw() {

    // Set the background color
    background(220);

    // Initialize the parameter
    let a = 5;
    let b = 7.7;
    let c = 0;
    let d = -5;

    // Call to log() function
    let v = log(a);
    let w = log(b);
    let x = log(c);
    let y = log(d);

    // Set the size of text
    textSize(16);

    // Set the text color
    fill(color('red'));

    // Getting natural log value
    text("Natural logarithm value of 5 is : " + v, 50, 30);
    text("Natural logarithm value of 7.7 is : " + w, 50, 50);
    text("Natural logarithm value of 0 is : " + x, 50, 70);
    text("Natural logarithm value of -5 is : " + y, 50, 90);

}
```

**输出:**

![](img/41b1f5200486286655289505eb7f6c4c.png)

**注意:**如果我们将输入作为负值，取零，那么它将输出分别作为“NaN”和-Infinity 返回。

**参考:**T2https://p5js.org/reference/#/p5/log