# 当给定的数字在使用 JavaScript 的范围内时，如何显示消息？

> 原文:[https://www . geeksforgeeks . org/如何使用 javascript 显示给定数字在范围之间时的消息/](https://www.geeksforgeeks.org/how-to-display-a-message-when-given-number-is-between-the-range-using-javascript/)

在本文中，我们将学习使用 JavaScript 在数字位于给定范围之间时显示一条消息。我们从用户那里获取一个数字，告诉用户它是否在一个范围内，在我们的例子中，范围是 1 到 10。

**方法:**我们创建一个按钮，并向其中添加一个[点击事件监听器](https://www.geeksforgeeks.org/javascript-addeventlistener-with-examples/)。当我们点击按钮时，浏览器屏幕上显示一个使用 JavaScript [*提示()*](https://www.geeksforgeeks.org/javascript-course-javascript-prompt-example/) 功能要求输入的提示。使用 JavaScript if-else 语句检查变量是否在该范围内。如果该输入在范围之间，我们使用*[*innerHTML*](https://www.geeksforgeeks.org/html-dom-innerhtml-property/)属性在屏幕上显示成功消息，否则，我们显示失败消息。*

*[**提示()方法:**](https://www.geeksforgeeks.org/javascript-window-prompt-method/)*

***语法:***

```html
*prompt("Message to show");*
```

***示例:***

## *超文本标记语言*

```html
*<!DOCTYPE html>
<html>

<head>
    <style>
        .gfg1 {
            font-size: 30px;
            color: green;
        }

        #gfg2 {
            font-size: 30px;
            color: green;
        }

        div {
            margin-left: 30%;
        }

        button {
            font-size: 20px;
        }
    </style>
</head>

<body>
    <div>
        <p class="gfg1">GeeksforGeeks</p>

        <button onclick="fun()">
            click me
        </button>

        <p id="gfg2"></p>
    </div>

    <script>
        function fun() {
            const input = prompt('Please enter a number:');

            if (input >= 1 && input <= 10)
                document.getElementById("gfg2")
                    .innerHTML = input + " Success!";
            else
                document.getElementById("gfg2")
                    .innerHTML = input + " Fail!"
        }
    </script>
</body>

</html>*
```

***输出:***

*<video class="wp-video-shortcode" id="video-587868-1" width="640" height="360" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20210411002950/bandicam-2021-04-11-00-27-00-728.mp4?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/20210411002950/bandicam-2021-04-11-00-27-00-728.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20210411002950/bandicam-2021-04-11-00-27-00-728.mp4)</video>*