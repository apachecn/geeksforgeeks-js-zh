# 使用 JavaScript 设计一个神经形态风格的数字钟

> 原文:[https://www . geeksforgeeks . org/design-a-digital-clock-in-neommorphism-style-use-JavaScript/](https://www.geeksforgeeks.org/design-a-digital-clock-in-neumorphism-style-using-javascript/)

时钟是用来测量时间的设备。如果使用得当，时钟对于任何用户界面都是一个有用的元素。时钟可以用在主要关注时间的网站上，比如一些订票网站或一些显示火车、公共汽车、航班等到达时间的应用程序。时钟基本上有两种，模拟和数字。在这里，我们将设计数字时钟，并添加一些造型，使其更具吸引力。

**方法:**方法是使用 date 对象获取每秒钟的时间，然后使用我们通过每秒钟调用相同函数获得的新时间在浏览器上重新渲染时间，并使时钟看起来更有吸引力。

**HTML & CSS 代码:**在这一节中，我们有一个以“HH:MM:SS”格式包装在“div”标签中的虚拟时间，并且我们已经在外部包含了 CSS 和 JavaScript 文件。

## HTML

```html
<!DOCTYPE html>
<html>

<head>
    <title>Digital clock</title>

    <style>

        /* Link for Google font */
        @import url(
'https://fonts.googleapis.com/css2?family=Orbitron&display=swap');

        body {

            /* Set background color of body */
            background-color: #afd275;

            /* Place item to center */
            align-items: center;
            display: flex;
            justify-content: center;

            /* Specify the vertical height */
            height: 100vh;
            overflow-y: hidden;
        }

        .clock {
            position: absolute;

            /* Put the clock content on
            center of the screen */
            top: 50%;
            left: 50%;
            transform: translateX(-50%) translateY(-50%);
            color: white;
            font-size: 60px;
            font-family: Orbitron;

            /* Provide space between letter of clock */
            letter-spacing: 7px;
            align-items: center;
            border-radius: 50px;
            display: flex;
            justify-content: center;
            margin-right: 4rem;
            height: 500px;
            width: 550px;

            /* Set the neumorphism effect to
             the body of clock */
            background-color: #afd275;
            box-shadow: inset 12px 12px 16px 0 rgba(0, 0, 0, 0.25),
                inset -8px -8px 12px 0 rgba(255, 255, 255, 0.3);
        }
    </style>
</head>

<body>
    <div class="container">
        <div id="MyClockDisplay"
            class="clock" onload="showTime()">
        </div>
    </div>

    <!-- Include JavaScript file -->
    <script src="index.js"></script>
</body>

</html>
```