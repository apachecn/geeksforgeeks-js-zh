# p5.js |光标()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-cursor-function/](https://www.geeksforgeeks.org/p5-js-cursor-function/)

p5.js 中的**光标()功能**用于将光标设置为预定义的符号或图像，如果已经隐藏，则使其可见。要将图像设置为光标，建议的大小为 16×16 或 32×32 像素。参数 x 和 y 的值必须小于图像的尺寸。

**语法:**

```
cursor(type, x, y)
```

**参数:**该功能接受三个参数，如上所述，描述如下:

*   **类型:**此参数存储光标的类型，如 ARROW、CROSS、HAND、MOVE、TEXT 和 WAIT Native CSS 属性:“抓取”、“进度”、“单元格”等。外部:光标图像的路径(允许的文件扩展名:。cur，。gif，。jpg，。jpeg，。巴布亚新几内亚)。
*   **x:** 此参数存储光标的水平活动点。
*   **y:** 此参数存储光标的垂直活动点。

下面的程序说明了 p5.js 中的 cursor()函数:

**示例:**本示例使用 cursor()函数显示光标。

```
function setup() {

    // Create canvas
    createCanvas(400, 400);

    // Set the text size
    textSize(40); 

    // Set the text alignment
    // to center
    textAlign(CENTER);
}

function draw() {
    cursor('https://s3.amazonaws.com/mupublicdata/cursor.cur');
}
```

**输出:**
![](img/3a5a18b5ac4903089450da29bc17c43a.png)

**参考:**T2】https://p5js.org/reference/#/p5/cursor