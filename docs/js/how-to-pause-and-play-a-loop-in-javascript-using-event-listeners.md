# 如何使用事件监听器在 JavaScript 中暂停和播放循环？

> 原文:[https://www . geeksforgeeks . org/如何使用事件侦听器暂停和播放 javascript 循环/](https://www.geeksforgeeks.org/how-to-pause-and-play-a-loop-in-javascript-using-event-listeners/)

下面给出的是一个用于 DOM 操作的 JavaScript 程序，基本上是关于**如何使用事件监听器在 JavaScript 中暂停和播放一个循环(不要和延迟混淆)**。在本文中，我们将 JavaScript 与 HTML 结合使用，因此我们需要一个网络浏览器，即 Chrome(推荐)或 Electron Application。在几乎所有编程语言中，暂停和播放循环都是一项非常困难的任务，并且没有简单的解决方案可以像我们在视频剪辑中所做的那样，在循环执行和再次点击按钮之间暂停循环，但是 JavaScript **Promise** 概念使暂停和播放循环与 DOM 元素的事件侦听器一起变得容易。这里暂停并播放循环**并不意味着**延迟一个循环。
如果您正在寻找 javascript 中的延迟循环，那么我们已经为它创建了一篇单独的文章，请访问:[https://www . geeksforgeeks . org/如何使用异步等待承诺来延迟 JavaScript 中的循环/](https://www.geeksforgeeks.org/how-to-delay-a-loop-in-javascript-using-async-await-with-promise/)

**方法:**我们在这个程序中暂停和播放循环的方法与使用**承诺**延迟循环相同，但是我们将通过事件侦听器**解决承诺，而不是在特定的持续时间后解决承诺。**在这段代码中，我们使用了一个名为 **Pauser** 的函数，该函数将暂停循环内的程序执行，我们还使用了一个变量 **stats** ，该变量的作用类似于暂停标志。
如果 stats 为 0，则暂停标志为假，如果 stats 为 1，则暂停标志为真，然后它将调用 Pauser()并等待事件侦听器得到解决。

**函数定义语法:**

## java 描述语言

```html
// This event listener will listen for 
// pause button click which will assign
// stats = 1 (means pause flag true)
document.getElementById("pa")
    .addEventListener("click", function () {
        stats = 1;
    })

function pauser() {
    return new Promise(resolve => {
        let playbuttonclick = function () {

            // Remove the event from play button
            // after clicking play button 
            document.getElementById("playbuttonelement")
                .removeEventListener("click", playbuttonclick);
            stats = 0;
            resolve("resolved");
        }

        // Here is the event listener for play
        // button (instead of setTimeout) which
        // will wait for the element to get click
        // to get resolved untill then it will be
        // remain stucked inside Promise 
        document.getElementById("playbuttonelement")
            .addEventListener("click", playbuttonclick)
    })
}
```