# p5.js Element removeClass()方法

> 原文:[https://www . geesforgeks . org/P5-js-element-remove class-method/](https://www.geeksforgeeks.org/p5-js-element-removeclass-method/)

p5 的 **removeClass()** 方法。p5.js 中的元素用于移除元素的指定类。一个元素可以分配多个类。此外，一个类可以指定给页面上的多个元素。

**语法:**

```
removeClass(class)

```

**参数:**该函数接受一个参数，如上所述，如下所述。

*   **类:**是表示要移除的类的字符串。

**示例:**下面的示例说明了 p5.js 中的 **removeClass()** 方法

## java 描述语言

```
function setup() {
  createCanvas(600, 300);
  textSize(18);

  text("Click on the buttons to add, remove " + 
       "or show the classes of the elements", 20, 20);

  setBtn = 
    createButton("Add given class to element");
  setBtn.position(30, 40);
  setBtn.mouseClicked(addClass);

  removeBtn = 
    createButton("Remove given class from element");
  removeBtn.position(30, 70);
  removeBtn.mouseClicked(removeClass);

  showBtn = createButton("Show current classes");
  showBtn.position(30, 100);
  showBtn.mouseClicked(showClasses);

  class_name = createInput('class1');
  class_name.position(30, 140);

  // Create a new p5.Element
  tmpElement = createElement("div");
}

function addClass() {
  clear();

  // Get the class to set
  let classToSet = class_name.value();

  // Set the class of the element
  tmpElement.addClass(classToSet);

  text("Class added with name: " + 
       classToSet, 20, 200);

  text("Click on the buttons to add, remove or " +
       "show the classes of the elements", 20, 20);
}

function removeClass() {
  clear();

  // Get the class to remove
  let classToRemove = class_name.value();

  // Remove the class of the element
  tmpElement.removeClass(classToRemove);

  text("Class removed with name: " +
       classToRemove, 20, 200);

  text("Click on the buttons to add, remove or " +
       "show the classes of the elements", 20, 20);
}

function showClasses() {
  clear();

  // Get the classes of the element
  let setClasses = tmpElement.class();

  // Display the classes
  if (setClasses != '')
    text("The classes of the element are: " +
         setClasses, 20, 180);
  else
    text("The element has no classes", 20, 180);

  text("Click on the buttons to add, remove or " +
       "show the classes of the elements", 20, 20);
}
```

**输出:**

![](img/83112bfb8a0dcc4096cfe5a7bfbc4775.png)

**在线编辑:**[【https://editor.p5js.org/】](https://editor.p5js.org/)
**环境设置:**[https://www . geeksforgeeks . org/P5-js-soundfile-object-installation-and-methods/](https://www.geeksforgeeks.org/p5-js-soundfile-object-installation-and-methods/)
**参考:**[https://p5js.org/reference/#/p5.Element/removeClass](https://p5js.org/reference/#/p5.Element/removeClass)