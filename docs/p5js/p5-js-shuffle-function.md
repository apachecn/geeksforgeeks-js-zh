# p5.js | shuffle()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-shuffle-function/](https://www.geeksforgeeks.org/p5-js-shuffle-function/)

p5.js 中的 **shuffle()函数**用于*对给定数组元素*的顺序进行洗牌。

**语法:**

```
shuffle(Array)
```

**参数:**该函数接受一个参数**数组**，其元素将被混洗。

**返回值:**返回混洗后的数组。

下面的程序说明了 p5.js 中的 shuffle()函数:
**示例-1:**

```
function setup() { 

    // Creating Canvas size
    createCanvas(500, 90); 

    // Set the background color 
    background(220); 

    // Initializing the arrays
    let Array1 = ['IT', 'CSE', 'ECE'];

    // Calling to shuffle() function.
    let Array2 = shuffle(Array1);

    // Set the size of text 
    textSize(16); 

    // Set the text color 
    fill(color('red')); 

    // Getting new shuffled array
    text("Shuffled array is : " + Array2, 50, 30);

} 
```

**输出:**
![](img/5ed4f13eb432ddaecce961c3ea4a5646.png)

**示例-2:**

```
function setup() { 

    // Creating Canvas size
    createCanvas(500, 90); 

    // Set the background color 
    background(220); 

        // Calling to shuffle() function on an array
        // Taken as the parameter
        let Array = shuffle(['Ram', 'Shayam', 'Geeta', 'Anita']);

    // Set the size of text 
    textSize(16); 

        // Set the text color 
    fill(color('red')); 

    // Getting new shuffled array
    text("Shuffled array is : " + Array, 50, 30);

} 
```

**输出:**
![](img/ff133afbbd1c777ac275f3af952c7bf5.png)

**注意:**在上面的代码中， **draw()函数**没有被使用，因为如果我们使用 draw 函数，那么它不会给出一个明确的输出，即它会不断地改变数组字符串的顺序，并且不会给出任何停滞的结果。

**参考:**T2】https://p5js.org/reference/#/p5/shuffle