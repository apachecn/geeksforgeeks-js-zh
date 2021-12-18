# 如何在 JavaScript 中不渲染引擎的情况下渲染列表？

> 原文:[https://www . geeksforgeeks . org/如何在没有 javascript 引擎渲染的情况下渲染列表/](https://www.geeksforgeeks.org/how-to-render-a-list-without-render-a-engine-in-javascript/)

Javascript 渲染引擎允许开发人员以固执己见的方式将原始 Javascript 数据渲染到网站中。这些例子有 [React](https://www.geeksforgeeks.org/reactjs-rendering-elements/) 、 [Vue](https://www.geeksforgeeks.org/vue-js-declarative-rendering/) 、Ember.js 和许多其他的。然而，这些框架并不需要*将 Javascript 数据渲染到网站中。*

在本文中，我们将获取一个字符串列表，并使用 DOM 和浏览器提供的 Javascript API 将它们呈现到一个简单的网站中。

**从一个基本的 HTML 文档开始:**让我们从创建一个简单的呈现空白页的 HTML 文档开始。现在，我们将回顾 DOM 规范定义的两种基本方法，这是将 Javascript 数据呈现到 DOM 中所必需的。

## HTML

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content=
        "width=device-width, initial-scale=1.0">
    <title>Geeks for Geeks</title>
</head>

<body></body>

</html>
```