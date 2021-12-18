# p5。元素 addClass()方法

> 原文:[https://www.geeksforgeeks.org/p5-element-addclass-method/](https://www.geeksforgeeks.org/p5-element-addclass-method/)

p5 的 **addClass()** 方法。p5.js 中的元素用于向元素添加指定的类。一个元素可以分配多个类。此外，一个类可以指定给页面上的多个元素。

**语法:**

```
addClass(class)
```

**参数:**该函数接受一个参数，如上所述，如下所述。

*   **类:**表示要添加的类的字符串。

**示例:**下面的示例说明了 p5.js 中的 **addClass()** 方法。

## java 描述语言

```
function setup() {
  createCanvas(550, 300);
  textSize(18);

  text("Click on the buttons to add the given " +
       "class to the element", 20, 20);

  setBtn =
    createButton("Add given class to element");
  setBtn.position(30, 40);
  setBtn.mouseClicked(addNewClass);

  setBtn =
    createButton("Show current classes");
  setBtn.position(300, 40);
  setBtn.mouseClicked(showClasses);

  class_name = createInput('class1');
  class_name.position(30, 80);

  // Create a new p5.Element
  tmpElement = createElement("div");
}

function addNewClass() {
  clear();

  // Get the class to set
  let classToSet = class_name.value();

  // Set the class of the element
  tmpElement.addClass(classToSet);

  text("Class added with name: " +
       classToSet, 30, 120);

  text("Click on the button to add the given " +
       "class to the element", 20, 20);
}

function showClasses() {
  clear();

  // Get the classes of the element
  let setClasses = tmpElement.class();

  // Display the classes
  text("The classes of the element are: " +
       setClasses, 30, 120);

  text("Click on the button to add the given " +
       "class to the element", 20, 20);
}
```

**输出:**

![](img/3cf7f5c3cde981df14360df924d3e476.png)

**在线编辑:**[【https://editor.p5js.org/】](https://editor.p5js.org/)
**环境设置:**[https://www . geeksforgeeks . org/P5-js-soundfile-object-installation-and-methods/](https://www.geeksforgeeks.org/p5-js-soundfile-object-installation-and-methods/)
**参考:**[https://p5js.org/reference/#/p5.Element/addClass](https://p5js.org/reference/#/p5.Element/addClass)