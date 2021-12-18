# 在 JavaScript 中去抖

> 原文:[https://www.geeksforgeeks.org/debouncing-in-javascript/](https://www.geeksforgeeks.org/debouncing-in-javascript/)

在 JavaScript 中去抖是一种用来提高浏览器性能的做法。网页中可能存在一些需要耗时计算的功能。如果频繁调用这样的方法，可能会极大地影响浏览器的性能，因为 JavaScript 是单线程语言。去抖是一种编程实践，用于确保耗时的任务不会频繁触发，从而影响网页的性能。换句话说，它限制了函数被调用的速率。

```
<html> 
<body>
<button id="debounce">
    Debounce
</button>
<script>
var button = document.getElementById("debounce");
const debounce = (func, delay) => {
    let debounceTimer
    return function() {
        const context = this
        const args = arguments
            clearTimeout(debounceTimer)
                debounceTimer
            = setTimeout(() => func.apply(context, args), delay)
    }
} 
button.addEventListener('click', debounce(function() {
        alert("Hello\nNo matter how many times you" +
            "click the debounce button, I get " +
            "executed once every 3 seconds!!")
                        }, 3000));
</script>
</body>
</html>
```

**输出:**3 秒后警报箱

```
Hello
No matter how many times you click the debounce button,
I get executed once every 3 seconds!!

```

**说明:**

该按钮附加到调用去抖功能的事件侦听器上。去抖功能有两个参数——一个函数和一个数字。
声明了一个变量去反跳定时器，顾名思义，用于实际调用函数，在“延迟”毫秒间隔后作为参数接收。
如果去抖按钮只被点击一次，那么去抖功能会在延迟后被调用。但是，如果点击一次去抖按钮，并在延迟结束前再次点击，初始延迟将被清除，新的延迟定时器将启动。clearTimeout 函数正被用来实现它。

去抖的一般思路是:
1。从 0 超时
2 开始。如果再次调用去抖功能，将计时器重置为指定的延迟
3。在超时的情况下，调用去反跳功能
因此每次调用去反跳功能时，都会重置计时器并延迟调用。

**应用:**
去抖可以应用于实现提示性文本，在这里我们等待用户停止输入几秒钟后再提示文本。因此，每次按键时，我们都会等待几秒钟，然后给出建议。
去抖的另一个应用是在内容加载网页，如脸书和推特，用户继续滚动。在这些场景中，如果滚动事件触发过于频繁，可能会影响性能，因为它包含大量视频和图像。因此滚动事件必须利用去抖。

JavaScript 最出名的是网页开发，但它也用于各种非浏览器环境。您可以通过以下 [JavaScript 教程](https://www.geeksforgeeks.org/javascript-tutorial/)和 [JavaScript 示例](https://www.geeksforgeeks.org/javascript-examples/)从头开始学习 JavaScript。