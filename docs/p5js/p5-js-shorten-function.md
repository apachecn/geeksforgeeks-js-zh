# P5 . js | short()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-shorten-function/](https://www.geeksforgeeks.org/p5-js-shorten-function/)

p5.js 中的**缩短()功能**用于*将给定数组的元素数量减少一个*。

**语法:**

```
shorten(Array)
```

**参数:**该函数接受一个参数**数组**，其元素要缩短一。

**返回值:**返回缩短后的数组。

下面的程序说明了 p5.js.
**中的 shorten()函数示例-1:**

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

    // Calling to shorten() function.
    let Array2 = shorten(Array1);

    // Set the size of text 
    textSize(16);

    // Set the text color 
    fill(color('red'));

    // Getting new shortened array
    text("Shortened array is : " + Array2, 50, 30);

}
```

**输出:**
![](img/99bcf9a4a057bc2f75714f46cfbe488a.png)

**示例-2:**

```
function setup() {

    // Creating Canvas size
    createCanvas(500, 90);
}

function draw() {

    // Set the background color 
    background(220);

    // Calling to shorten() function on an array
    // Taken as the parameter
    let Array = shorten(['Ram', 'Shayam', 'Geeta', 'Anita']);

    // Set the size of text 
    textSize(16);

    // Set the text color 
    fill(color('red'));

    // Getting new shortened array
    text("Shortened array is : " + Array, 50, 30);

}
```

**输出:**
![](img/ea03c17d06028a716fb7df8d5ba6a04b.png)

**参考:**T2】https://p5js.org/reference/#/p5/shorten