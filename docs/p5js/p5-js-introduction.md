# p5.js |简介

> 原文:[https://www.geeksforgeeks.org/p5-js-introduction/](https://www.geeksforgeeks.org/p5-js-introduction/)

p5.js 是一个用于创造性编码的 JavaScript 库。它基于[处理](https://processing.org/)，这是一个创造性的编码环境。处理的主要重点是使初学者尽可能容易地学习如何编写交互式图形应用程序，通过可视化使编程语言更加用户友好。
使用 JavaScript 编程语言的优势在于其广泛的可用性和无处不在的支持:每个网络浏览器都内置了 JavaScript 解释器，这意味着 p5.js 程序可以在任何网络浏览器上运行。
另外，Processing 是一种强调可行性的语言，程序员可以非常快速地创建软件原型，尝试一个新的想法，或者看看某件事是否可行。因此，处理(和 p5.js)程序通常被称为“草图”

**首选编辑器**P5 . js 的官方文档建议使用括号或崇高，然后包含 JavaScript 文件，最终引导我们像任何其他编程语言一样工作。但是在线 p5.js 网络编辑器是最好的选择。它基于一个基于网络的编程环境。

【P5.js 和 JavaScript 的区别？
JavaScript 是一种核心语言，它提供了在浏览器中构建任何功能的所有特性。它可以使用循环、函数、条件、DOM 操作、事件、画布等。因此，通过使用它来开发和设计任何框架。
p5.js 是一个 JavaScript 库。P5.js 运行在 Pure JavaScript 上提供了一些功能，使得 JavaScript 用户的生活在 web 中很容易画出来。

**示例:**

```
function setup() {
  createCanvas(400, 400); //Canvas size 400*400
}

function draw() {
  background('blue'); //background color blue
}
```

**输出:**
![](img/7bd8378478f95051edfbfb99c8885cab.png)

**setup():** 是 setup()函数中的语句。它在程序开始时执行一次。createCanvas 必须是第一条语句。
**draw():**draw()中的语句一直执行到程序停止。每个语句按顺序执行，读取最后一行后，第一行将再次执行。

**参考:**T2】https://p5js.org/

**Credits:**

*   劳伦·麦卡锡(p5.js 的创造者)*   Cassie Tarakajian(P5 . js 网页编辑器的创建者)