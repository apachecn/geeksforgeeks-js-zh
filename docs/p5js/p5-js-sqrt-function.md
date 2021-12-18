# p5.js | sqrt()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-sqrt-function/](https://www.geeksforgeeks.org/p5-js-sqrt-function/)

p5.js 中的 **sqrt()函数**用于获取任意输入数的平方根。

**语法:**

```
sqrt(n)
```

**参数:**此函数接受单参数 **n** ，这是一个输入的非负数，其平方根正在计算中。

**返回值:**返回任意输入数的平方根。

下面的程序说明了 p5.js 中的 sqrt()函数:

**示例:**本示例使用 sqrt()函数获取输入数字的平方根。

```
function setup() { 

    // Create Canvas of size 270*80 
    createCanvas(350, 80); 
} 

function draw() { 

    // Set the background color 
    background(220); 

    // Initialize the parameter 
    let a = 25; 
    let b = 16; 

    // Call to sqrt() function 
    let x = sqrt(a);
    let y = sqrt(b); 

    // Set the size of text 
    textSize(16); 

    // Set the text color 
    fill(color('red')); 

    // Getting output
    text("Square root of 25 is: " + x, 50, 30);
    text("Square root of 16 is: " + y, 50, 50); 
} 
```

**输出:**
![](img/10ecb2fa5332bc9f94ddbfe79d9c31ae.png)

**参考:**T2】https://p5js.org/reference/#/p5/sqrt