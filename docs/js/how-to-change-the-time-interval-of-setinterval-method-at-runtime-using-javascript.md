# 如何用 JavaScript 在 RunTime 改变 setinterval()方法的时间间隔？

> 原文:[https://www . geeksforgeeks . org/如何使用 javascript 在运行时更改 setinterval 方法的时间间隔/](https://www.geeksforgeeks.org/how-to-change-the-time-interval-of-setinterval-method-at-runtime-using-javascript/)

在本文中，我们将学习如何在运行一个元素后更改 setInterval()时间。setInterval()方法读取一次计时，并定期调用函数。下面讨论解决这个问题的两种方法:
**方法 1:使用 clearInterval()方法:**setInterval()方法返回一个数字 ID。这个标识可以传递给 clearInterval()方法来清除/停止 setInterval 定时器。在这种技术中，我们在每个 setInterval()之后继续激发 clearInterval()，以停止之前的 setInterval()，并用新的计数器初始化 setInterval()。
**例:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        How to Change the Time Interval of
        setinterval() Method after Running
        one Element using JavaScript ?
    </title>
</head>

<body>
    <div id="message"></div>

    <script>

        // Output message
        var msg = document.getElementById("message");

        var t = 200; // Timer

        // Stores the setInterval ID used by
        // clearInterval to stop the timer
        var interval;

        f1();

        // Function that changes the timer
        function changeTimer(){
            t = t * 1.2;
        }

        // Function that run at irregular intervals
        function f1() {

            // Clears the previous setInterval timer
            clearInterval(interval);
            msg.innerHTML += "
<p>Function Fired</p>
";
            changeTimer();
            interval = setInterval(f1, t);
        }
    </script>
</body>

</html>
```

**输出:**

![output](img/5251c83eb7e28a2869396671d222552e.png)

**方法二:使用 setTimeout()方法:**这种技术比前一种更简单易行。setTimout()方法在一定时间后触发一个函数。计时器是我们想要运行功能的时间。在这种技术中，在执行了所需的任务之后，我们更改计时器的值，并再次调用 setTimeout()。现在，由于定时器的值改变，每个函数调用在不同的时间间隔被调用。
**例:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        How to Change the Time Interval of
        setinterval() Method after Running
        one Element using JavaScript ?
    </title>
</head>

<body>
    <div id="message"></div>
    <script>

        // To display output
        var msg = document.getElementById("message");

        // Timer
        var t = 200;

        f1();

        // Function that changes the timer
        function changeTimer(){
            t = t * 1.2;
        }

        // Function to run at irregular intervals
        function f1() {
            msg.innerHTML += "
<p>Function Fired</p>
";
            changeTimer();
            setTimeout(f1, t);
        }
    </script>
</body>

</html>
```

**输出:**

![output](img/5251c83eb7e28a2869396671d222552e.png)