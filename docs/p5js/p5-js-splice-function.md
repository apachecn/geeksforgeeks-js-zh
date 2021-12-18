# p5.js |拼接()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-splice-function/](https://www.geeksforgeeks.org/p5-js-splice-function/)

p5.js 中的**拼接()函数**用于在给定数组中插入值或数组元素。
**语法:**

```
splice(Array, Values, Position)
```

**参数:**该功能接受三个参数，如上所述，描述如下:

*   **数组:**这是一个要修改的给定数组。
*   **值:**这是另一个数组的值，该数组的元素将被插入到要修改的给定数组中。
*   **位置:**这是给定数组的元素数，在此之后将插入另一个数组的新值或元素。

**返回值:**返回一个新的修改后的数组。
下面的程序说明了 p5.js:
**中的 splice()函数示例 1:** 本示例使用 splice()函数在给定数组中插入值或数组元素。

## java 描述语言

```
function setup() {

    // Creating Canvas size
    createCanvas(500, 90);
}

function draw() {

    // Set the background color
    background(220);

    // Initializing the array
    let Array = [9, 6, 0, 22, 4, 1, 15];

    // Initializing the value which are
    // to be inserted
    let Value = 5;

    // Initializing the position after
    // which insertion is done
    // counting is done from starting
    let Position = 5;

    // Calling to splice() function.
    let A = splice(Array, Value, Position);

    // Set the size of text
    textSize(16);

    // Set the text color
    fill(color('red'));

    // Getting new modified array
    text("New modified array is : " + A, 50, 30);          
}
```