# p5.js | concat()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-concat-function/](https://www.geeksforgeeks.org/p5-js-concat-function/)

p5.js 中的 **concat()函数**用于连接两个给定的数组。这个函数从未来的版本中折旧，改为使用 First _ array . concat(Second _ array)。

**语法:**

```
concat(First_array, Second_array)
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **First_array:** 将与第二个数组串联的第一个数组。
*   **Second_array:** 将与第一个数组连接的第二个数组。

**返回值:**返回一个新的串联数组。

下面的程序说明了 p5.js 中的 concat()函数:

**示例:**本示例使用 concat()函数连接两个数组。

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

    // Calling to concat() function.
    let Array3 = concat(Array1, Array2);

    // Set the size of text 
    textSize(16); 

    // Set the text color 
    fill(color('red')); 

    // Getting new concatenated array
    text("New concatenated array is : " 
            + Array3, 50, 30);
} 
```

**输出:**
![](img/8c2caf836a1be6c54f06647f57d4e929.png)

**参考:**T2】https://p5js.org/reference/#/p5/concat