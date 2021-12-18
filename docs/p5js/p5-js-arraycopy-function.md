# p5.js | arrayCopy()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-arraycopy-function/](https://www.geeksforgeeks.org/p5-js-arraycopy-function/)

p5.js 中的 **arrayCopy()函数**用于将一部分源数组元素复制到另一个目标数组中。该功能从未来版本中折旧。

**语法:**

```
arrayCopy( src, src_pos, dst, dst_pos, length )
```

**参数:**该功能接受五个参数，如上所述，描述如下:

*   **src:** 这是要将元素复制到另一个数组中的源数组。
*   **src_pos:** 这是复制元素的源数组元素的位置。
*   **dst:** 这是复制的源数组元素要粘贴到的目标数组。
*   **dst_pos:** 这是目标数组的位置，源数组元素要粘贴在这里。
*   **长度:**这是要从源数组复制的元素数。

**返回值:**返回新复制的目的数组。
下面的程序说明了 p5.js 中的 arrayCopy()函数:
**示例 1:** 本示例使用 arrayCopy()函数将源数组元素复制到目标数组。

## java 描述语言

```
function setup() {

    // Creating Canvas of given size
    createCanvas(500, 90);
}

function draw() {

    // Set the background color
    background(220);

    // Initializing the source array
    let src = ['IT', 'CSE', 'ECE'];

    // Initializing the source array position
    // from where the elements are to be copied.
    let src_pos = 1;

    // Initializing the destination array
    let dst = ['Ram', 'Shyam', 'Geeta'];

    // Initializing the destination position
    // where copied elements are to be pasted.
    let dst_pos = 0;

    // Initializing the number of source array elements
    // which are to be copied.
    let length = 2;

    // Calling to arrayCopy() function.
    arrayCopy(src, src_pos, dst, dst_pos, length);

    // Set the size of text
    textSize(16);

    // Set the text color
    fill(color('red'));

    // Getting new destination array
    text("New destination array is : " + dst, 50, 30);

}
```

**输出:**

![](img/9e78f40787350ea0f2d72a8166e2c624.png)

**示例 2:** 本示例使用 arrayCopy()函数将源数组元素复制到目标数组。

## java 描述语言

```
function setup() {

    // Creating Canvas of given size
    createCanvas(500, 90);
}

function draw() {

    // Set the background color
    background(220);

    // Initializing the source array
    let src = ['geeks', 'Students', 'Teachers'];

    // Initializing the source array position
    // from where the elements are to be copied.
    let src_pos = 2;

    // Initializing the destination array
    let dst = ['A', 'B', 'C'];

    // Initializing the destination position
    // where copied elements are to be pasted.
    let dst_pos = 1;

    // Initializing the number of source array elements
    // which are to be copied.
    let length = 1;

    // Calling to arrayCopy() function
    arrayCopy(src, src_pos, dst, dst_pos, length);

    // Set the size of text
    textSize(16);

    // Set the text color
    fill(color('red'));

    // Getting new destination array
    text("New destination array is : " + dst, 50, 30);
}
```

**输出:**

![](img/a5076669f181c703d691fa25b666ea23.png)

**参考:**T2https://p5js.org/reference/#/p5/arrayCopy