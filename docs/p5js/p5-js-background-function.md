# p5.js |后台()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-background-function/](https://www.geeksforgeeks.org/p5-js-background-function/)

p5.js 中的**背景()功能**用于设置 p5.js 画布背景使用的颜色。默认背景是透明的。根据当前颜色模式，该功能接受的颜色可以是 RGB、HSB 或 HSL 颜色。

**语法:**

```
background(c)
```

**参数:**该功能接受存储 p5 的单参数 **c** 。颜色对象、颜色组件或 CSS 颜色。

下面的程序说明了 p5.js 中的 background()函数:

**示例 1:** 本示例使用 background()函数设置背景颜色。

```
function setup() {

    // Create Canvas of size 300*300
    createCanvas(300, 300);
}

function draw() {
    background(220, 141, 155); //RGB Value
}
```

**输出:**
![](img/d9bdb7ee8018961c97437acd73c3f0a0.png)

**示例 2:** 本示例使用 background()函数设置背景颜色。

```
function setup() {

    // Create Canvas of size 300*300
    createCanvas(300, 300);
}

function draw() {

    // Set background color to green
    background('green');
}
```

**输出:**
![](img/11bb7cb117067cab60d08e10acb2a796.png)

**参考:**T2】https://p5js.org/reference/#/p5/background