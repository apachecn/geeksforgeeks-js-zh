# 如何用 JavaScript 创建即将到来的页面？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 创建即将到来的页面/](https://www.geeksforgeeks.org/how-to-create-a-coming-soon-page-using-javascript/)

#### 什么即将到来的一页？

首先，我们需要知道**即将到来的页面**是什么意思，**即将到来的**是一个术语，意思是即将如期发生或预计在不久的将来发生的事情。由此，我们得出结论:**即将到来 Pag <u>e</u>** 是一种网页类型，用于宣传以及告知潜在的观众网站页面上接下来会发生什么。(例如:电子商务网站上弹出的新智能手机页面。在本文中，我们将讨论如何创建一个即将到来的页面。

**即将到来页面功能:**

1.  作为一个观众，我们必须思考我们想在我们正在访问的特定页面上看到什么，以及页面在设计和内容方面对我们有多大吸引力。
2.  我们应该对我们向观众展示的内容有一个完整的了解。(例如:-对于有机食品，我们将选择自然和食物的主题。
3.  当你创建你的即将到来的页面时，一定要把倒计时天数。所以，观众会知道产品什么时候推出。
4.  一定要把 WATCH LATER 和 SHARE 链接选项放在页面上，这样如果观众想以后再看这个页面或者尽可能和其他人共享这个页面。

**进场:**

*   首先使用图像或画布设置网页的背景。
*   使用 [Date()](https://www.geeksforgeeks.org/javascript-date-objects/) 设置启动日期。
*   使用 [setinterval()](https://www.geeksforgeeks.org/java-script-settimeout-setinterval-method/) 更新 var x 中每秒的计数。
*   计算天、小时、分钟和秒
*   显示结果

#### 示例:

## 超文本标记语言

```html
<!DOCTYPE HTML>
<HTML>
<style>
    header {
        background-image: url(
https://media.geeksforgeeks.org/wp-content/cdn-uploads/20210908212955/Get-Hired-With-GeeksforGeeks-GFG-Job-Portal.png);
        background-position: center;
        height: 100vh;
        background-size: 100% 96%;
    }

    .Tech {
        top: 19%;
        left: 50%;
        position: absolute;
        transform: translate(-50%, -50%);
        color: rgb(20, 158, 212);
        text-align: center;
        font-size: 17px;
    }

    #Release {
        color: white;
        font-size: 40px;
        word-spacing: 10px;
    }
</style>

<head>
    <link href="style.css" 
          rel="stylesheet" 
          type="text/css">
</head>

<BODY>
    <header>
        <div class="Tech">
            <h2>COMING SOON</h2>

            <p id="Release"></p>

        </div>
    </header>

    <script>
        // Set the date of launching
        var RemainingTime = new Date("Feb 17, 2022 00:00:00");

        var RemainingTime = RemainingTime.getTime();

        // Update the count down every second
        var x = setInterval(function() {

            // Get current date and time
            var now = new Date().getTime();
            var distance = RemainingTime - now;

            // Days, hours, minutes and seconds time calculations
            var days_remaining =
                 Math.floor(distance / (1000 * 60 * 60 * 24));
            var hours_remaining = 
                 Math.floor(days_remaining / (1000 * 60 * 60));
            var x1 = distance % (1000 * 60 * 60);
            var minutes = Math.floor(x1 / (1000 * 60));
            var x2 = distance % (1000 * 60);
            var seconds = Math.floor(x2 / 1000);

            // Display the results
            document.getElementById("Release").innerHTML =
                days_remaining +
                " : " + hours_remaining + " : " + minutes +
                " : " + seconds;

            // Text after count down is over
            if (distance < 0) {
                clearinterval(x);
                document.getElementById("Release").
                innerHTML = "Welcome";
            }

        }, 1000);
    </script>
</BODY>

</HTML>
```

**输出:**

![](img/c488304666d1e30b403f000e34d1d13c.png)