# p5.js | splitTokens()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-splittokens-function/](https://www.geeksforgeeks.org/p5-js-splittokens-function/)

p5.js 中的 **splitTokens()函数**用于使用分隔符将输入字符串分割成数据段。该分隔符可以是输入字符串各部分之间使用的任何字符串或符号。
**语法:**

```
splitTokens( string, delimiter )
```

**参数:**该功能接受两个参数，如上所述，描述如下:

*   **字符串:**这是要拆分的输入字符串。
*   **分隔符:**这是用于分隔输入字符串数据的任何字符串或符号。

**返回值:**返回用逗号(，)分隔的输入字符串的拆分数据。
下面的程序说明了 p5.js:
**中的 splitTokens()函数示例 1:** 本示例使用 splitTokens()函数，使用分隔符将输入字符串分割成数据段。

## java 描述语言

```
function setup() {

    // Create Canvas
    createCanvas(500, 60);
}
function draw() {

    // Set the background color
    background(220);

    // Initializing the Strings
    let String = 'GeeksforGeeks/Geeks/Geek/gfg'; 

    // Calling to splitTokens() function
    let A = splitTokens(String, '/');

    // Set the size of text
    textSize(16);

    // Set the text color
    fill(color('red'));

    // Getting splitted string
    text("Splitted string is: " + A, 50, 30); 
}
```