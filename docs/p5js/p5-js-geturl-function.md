# p5.js | getURL()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-geturl-function/](https://www.geeksforgeeks.org/p5-js-geturl-function/)

p5.js 中的 getURL()函数用于返回当前的 URL。

**语法:**

```
getURL()
```

**参数:**此功能不接受任何参数。

**返回值:**返回当前网址字符串。

下面的程序说明了 p5.js 中的 getURL()函数:

**示例:**

```
// Declare a URL variable
let url;

// Function to set the height and
// width of window
function setup() {
    createCanvas(350, 200);

    // Use getURL() function to
    // get the current URL
    url = getURL();
}

function draw() {

    // Set the background color
    background(0, 200, 0);

    // Set the font-size
    textSize(30);

    // Set the text alignment
    textAlign(LEFT);

    text(url, 100, height / 2);
}
```

**输出:**
![](img/af458d77d146528fbceead0dedd2f287.png)

**参考:**T2】https://p5js.org/reference/#/p5/getURL