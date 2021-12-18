# p5.js | createSelect()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-createselect-function/](https://www.geeksforgeeks.org/p5-js-createselect-function/)

p5.js 中的 **createSelect()函数**用于在 DOM(文档对象模型)中创建一个下拉菜单元素，用于输入。那个。value()方法用于获取所选选项。这个函数包括 p5.dom 库。在标题部分添加以下语法。

**注意:**这个函数需要 p5.dom 库。因此，在 index.html 文件的头部添加下面一行。

**语法:**

```
createSelect(multiple)
```

或者

```
createSelect(existing)
```

**参数:**

*   **倍数:**保持输入状态。多如果*真*，单如果*假*。
*   **现有:**保存对象 DOM 选择元素。

**返回值:**该函数返回 p5 中某个属性的值。元素格式。

**示例:**本示例使用下拉菜单来更改给定选项的背景颜色。

## java 描述语言

```
// Create a variable for dropdown menu object
var dropdown;

function setup() {
    // Create a canvas
    createCanvas(400,400);
    // Create a dropdown menu object
    dropdown = createSelect();
    // Position the dropdown menu
    dropdown.position(150,200);
    // Set options
    dropdown.option("orange");
    dropdown.option("green");
    dropdown.option("skyblue");
}

function draw() {
    // Set the background-color as chosen
    // from the dropdown menu
    background(dropdown.value());
}
```

**输出:**

*   在改变颜色之前:

![](img/75bc2c4226eecb62a178fd63b1ae5b99.png)

*   在改变颜色的过程中:

![](img/ccd581388308133d842cdfc865fcda1c.png)

*   更改颜色后:

![](img/51143f488f5827efed1fc599d876dd17.png)

**在线编辑:**[【https://editor.p5js.org/】](https://editor.p5js.org/)
**环境设置:**[https://www . geeksforgeeks . org/P5-js-soundfile-object-installation-and-methods/](https://www.geeksforgeeks.org/p5-js-soundfile-object-installation-and-methods/)

**参考:**T2https://p5js.org/reference/#/p5/createSelect