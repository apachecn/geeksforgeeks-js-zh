# JavaScript 为什么不支持多线程？

> 原文:[https://www . geesforgeks . org/why-nots-JavaScript-support-多线程/](https://www.geeksforgeeks.org/why-doesnt-javascript-support-multithreading/)

**什么是多线程？**
多线程是一种执行模型，它允许不同的线程存在于一个进程的设置中，最终目标是它们自主执行但共享它们的进程资源。一个线程会记录对其执行很重要的数据，包括优先级调度、异常处理程序、一组中央处理器寄存器以及其宿主进程位置空间中的堆栈状态。

**JavaScript 为什么不支持？**
你可能知道，JavaScript 是**单线程**。为了更好地解释，这意味着一个单线程处理事件循环。对于更成熟的浏览器，整个浏览器在每个选项卡之间共享一个线程。当今的浏览器通过利用[每个站点的进程案例](https://www.chromium.org/developers/design-documents/process-models)或每个标签的不同线程来增强这一点。尽管专用线程提高了页面的响应速度，但它使每个选项卡都无法处理同时运行的不同脚本。
事实上，即使是谷歌 Chrome 也不会让一个单独网站页面的 JavaScript 同时运行，理由是这会在现有网页中造成巨大的并发问题。Chrome 所做的只是将各种组件(各种选项卡、模块等)分成离散的进程，然而没有人能想象一个单独的页面有一个以上的 JavaScript 线程。