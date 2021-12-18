# p5.js | reverse()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-reverse-function/](https://www.geeksforgeeks.org/p5-js-reverse-function/)

p5.js 中的**反转()功能**用于*反转给定数组元素*的顺序。

**语法:**

```
reverse(Array)
```

**参数:**该函数接受一个参数**数组**，其元素将被反转。

**返回值:**返回一个新的反转数组。

下面的程序举例说明了 p5.js:
**中的 **reverse()函数**示例:**本示例使用 reverse()函数来**反转给定数组元素的顺序**。

```
function setup() { 

    // Creating Canvas size
    createCanvas(500, 90); 
} 

function draw() { 

    // Set the background color 
    background(220); 

    // Initializing the arrays
    let Array1 = ['IT', 'CSE', 'ECE'];
        let Array2 = ['Civil', 'Mechanical'];

        // Calling to reverse() function.
        let Array3 = reverse(Array1);
        let Array4 = reverse(Array2);

    // Set the size of text 
    textSize(16); 

        // Set the text color 
    fill(color('red')); 

    // Getting new reversed array
    text("First reversed array is : "
      + Array3, 50, 30);
        text("Second reversed array is : " 
      + Array4, 50, 50);            
} 
```

**输出:**
![](img/6807a67e0f49482aa4037aeca7064999.png)

**参考:**T2】https://p5js.org/reference/#/p5/reverse