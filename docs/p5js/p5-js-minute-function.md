# p5.js |分钟()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-minute-function/](https://www.geeksforgeeks.org/p5-js-minute-function/)

p5.js 中的**分钟()功能**用于返回系统时钟中的当前分钟。minute()函数的值介于 0 到 59 之间。

**语法:**

```
minute()
```

**参数:**函数不接受任何参数。

**返回值:**该函数返回一个代表分钟时间的整数值。

下面的程序说明了 p5.js 中的 minute()函数:

**示例:**本示例使用 minute()函数返回系统时钟中的当前分钟。

```
function setup() {

    // Create Canvas of size 270*80
    createCanvas(270, 80);
}

function draw() {

    // Set the background color
    background(220);

    // Initialize the parameter with 
    // current minute
    let m = minute();

    // Set the text font size
    textSize(16);

    // Set the text color
    fill(color('red'));

    // Display the result
    text("Current minute is : "+m, 50, 30);
}
```

**输出:**
![](img/18ddf7c91abe9bf6282f1a3a272ba5be.png)

**参考:**T2】https://p5js.org/reference/#/p5/minute