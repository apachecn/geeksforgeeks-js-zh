# p5.js createElement()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-createelement-function/](https://www.geeksforgeeks.org/p5-js-createelement-function/)

**createElement()** 函数用于在 DOM(文档对象模型)中创建一个元素。**。位置()**功能用于设置元素的位置。

**注意:**这个函数需要 p5.dom 库。所以在**index.html**文件的头部增加下面一行。

> >

**语法:**

```
createElement( tag, [content] )
```

**参数:** 该功能接受两个参数，如上所述，描述如下:

*   **标记:**该参数保存新元素的标记。
*   **内容:**此参数保存要插入元素的 html 内容

**返回值:**返回一个指针元素，保存创建的节点对象。

**示例:** 本示例使用 createElement()函数创建元素。

## java 描述语言

```
function setup() {
  // create canavas
  createCanvas(400, 400);
}

function draw() {
  // set background color
  background(150, 255, 134);
  // create the element
  create_element = createElement('h1', ["GeeksForGeeks!"]);

  // position the element
  create_element.position(50, 100);

}
```

**输出:**

![](img/b99f89b2cb28dda0563d94b13f13053a.png)

**参考:**T2https://p5js.org/reference/#/p5/createElement