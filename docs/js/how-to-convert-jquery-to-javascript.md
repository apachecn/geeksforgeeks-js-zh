# 如何将 jQuery 转换成 JavaScript？

> 原文:[https://www . geesforgeks . org/how-convert-jquery-to-JavaScript/](https://www.geeksforgeeks.org/how-to-convert-jquery-to-javascript/)

**[JavaScript](https://www.geeksforgeeks.org/javascript-tutorial/)** 是一种面向对象的编程语言，旨在使 web 开发变得更容易、更有吸引力。在大多数情况下，JavaScript 用于为网页创建响应性的交互式元素，从而增强用户体验。

**[jQuery](https://www.geeksforgeeks.org/jquery-tutorials/)** 是一个开源的 JavaScript 库，它简化了 HTML/CSS 文档，或者更准确地说是文档对象模型(DOM)和 JavaScript 之间的交互。

**选择:**在 jQuery 中，要选择任意元素，我们只需使用 **$()** 符号，但在 JavaScript 中，要选择任意元素，我们可以使用 [**querySelector()**](https://www.geeksforgeeks.org/html-dom-queryselector-method/) 或[**query selectorall()**](https://www.geeksforgeeks.org/html-dom-queryselectorall-method/)。

*   **程序:**

    ```
    // jQuery to select all instances
    // of class "select"
    $(".select");

    // JavaScript to select only the
    // first instance of class "select"
    document.querySelector(".select");

    // To select all the instances
    // of class "select"  
    document.querySelectorAll(".select");
    ```

选择器的其他一些例子:

**选择整个 html:**

*   在 jQuery 中:

    ```
    $("html")
    ```

*   在 JavaScript 中:

    ```
    document.querySelector(selector)
    ```

**选择整个 html 正文:**

*   在 jQuery 中:

    ```
    $("body")
    ```

*   在 JavaScript 中:

    ```
    document.body
    ```

**类操控:**

*   **程序:**

    ```
    // To add a class "class-name" to a <p> tag
    // jQuery:
    $p.addClass(class-name) 

    // JavaScript:
    p.classList.add(class-name)
    ```

下面是一些其他的操作示例:

**向 html 元素添加类:**

*   在 jQuery 中:

    ```
    $element.addClass(class-name)
    ```

*   在 JavaScript 中:

    ```
    element.classList.add(class-name)
    ```

**移除 html 元素的类:**

*   在 jQuery 中:

    ```
    $element.removeClass(class-name)
    ```

*   在 JavaScript 中:

    ```
    element.classList.remove(class-name)
    ```

**将类切换到 html 元素:**

*   在 jQuery 中:

    ```
    $element.toggleClass(class-name)
    ```

*   在 JavaScript 中:

    ```
    element.classList.toggle(class-name)
    ```

**检查 html 元素是否包含类:**

*   在 jQuery 中:

    ```
    $element.hasClass(class-name)
    ```

*   在 JavaScript 中:

    ```
    element.classList.has(class-name)
    ```

**事件监听器**

*   **程序:**

    ```
    // To add an event on button click

    // jQuery:
    /* handle click event */  
    $(".button").click( function(event) { 
    });

    // JavaScript:
    /* handle click event */  
    document.querySelector(".button")
        .addEventListener("click", (event) => {
    });
    ```

**CSS 造型:**

*   **程序:**

    ```
    // To give a margin of 10px to all the div
    // jQuery:
    $div.css({ margin: "10px" }) 

    // JavaScript:
    div.style.margin= "10px"
    ```

jQuery 是一个开源的 JavaScript 库，它简化了 HTML/CSS 文档之间的交互，它以其“少写多做”的理念而闻名。
跟随本 [jQuery 教程](https://www.geeksforgeeks.org/jquery-tutorials/)和 [jQuery 示例](https://www.geeksforgeeks.org/jquery-examples/)可以从头开始学习 jQuery。