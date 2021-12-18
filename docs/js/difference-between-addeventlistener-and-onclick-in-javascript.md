# JavaScript 中 addEventListener 和 onclick 的区别

> 原文:[https://www . geesforgeks . org/addeventlistener-and-onclick-in-JavaScript/](https://www.geeksforgeeks.org/difference-between-addeventlistener-and-onclick-in-javascript/)之间的区别

**addEventListener()** 和 **onclick** 都在监听一个事件。两者都可以在单击按钮时执行回调函数。然而，它们并不相同。在本文中，我们将了解它们之间的差异。

[**addEventListener()**](https://www.geeksforgeeks.org/javascript-addeventlistener-with-examples/)**:****addEventListener()**方法将事件处理程序附加到指定的元素。

**语法:**

```
element.addEventListener(event, listener, useCapture);
```

**参数:**

*   **事件:**事件可以是任何有效的 JavaScript 事件。使用不带“on”前缀的事件，如使用“click”而不是“onclick”或“mousedown”而不是“onmousedown”。
*   **监听器(处理函数):**它可以是一个响应发生的事件的 JavaScript 函数。
*   **使用捕获:**(可选参数)一个布尔值，指定事件应该在捕获阶段还是在冒泡阶段执行。

**注意:**addEventListener()方法可以对同一个元素应用多个事件处理程序。它不会覆盖其他事件处理程序。

**示例:**下面是一个 JavaScript 代码，显示多个事件与一个元素相关联，并且没有覆盖。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<body>
    <button id="btn">Click here</button>
    <h1 id="text1"></h1>
    <h1 id="text2"></h1>

    <script>
        let btn_element = document.getElementById("btn");

        btn_element.addEventListener("click", () => {
            document.getElementById("text1")
                .innerHTML = "Task 1 is performed";
        })

        btn_element.addEventListener("click", () => {
            document.getElementById("text2")
                .innerHTML = "Task 2 is performed";
        });
    </script>
</body>

</html>
```

**输出:**

![](img/54c7b281f153c37607f7b1a761cc255c.png)

[**onclick**](https://www.geeksforgeeks.org/html-dom-onclick-event/)**:****onclick**事件属性在用户点击按钮时生效。当鼠标点击元素时，脚本运行。

**语法:**

[**HTML 中:**](https://www.geeksforgeeks.org/html-onclick-event-attribute/)

```
<element onclick="myScript">
```

**在 JavaScript 中:**

```
object.onclick = function(){myScript};
```

**onclick** 只是一个属性。像所有对象属性一样，如果我们编写多个属性，它将被覆盖。

**示例:**下面是一个 JavaScript 代码，显示了多个事件不能与一个元素相关联，因为存在覆盖

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<body>
    <button id="btn">Click here</button>
    <h1 id="text1"></h1>
    <h1 id="text2"></h1>

    <script>
        let btn_element = document.getElementById("btn");

        btn_element.onclick = () => {
            document.getElementById("text1")
                .innerHTML = "Task 1 is performed";
        };

        btn_element.onclick = () => {
            document.getElementById("text2")
                .innerHTML = "Task 2 is performed";
        };
    </script>
</body>

</html>
```

**输出:**

![](img/2a55cad4d070a55d0686c9e65a5d71de.png)

**addevent listener 与 onclick 的区别:**

<figure class="table">

| **addevent listener** | **onclick** |
| Addevent listener can add multiple events to a specific element. | Onclick can only add a single event to an element. It is basically an attribute, so it will be overwritten. |
| AddEventListener can take the third parameter, which can control the event propagation. | Onclick cannot control the event propagation. |
| Addlistener can only be added in JavaScript files inside or outside the element. | Onclick can also be added as an HTML attribute. |
| addevent listener(addevent listener)哦，亲爱的 internet explorer(internet explorer)朱庇特？朱庇特，哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟系好安全带云娥。 | Onclick works in all browsers. |

</figure>