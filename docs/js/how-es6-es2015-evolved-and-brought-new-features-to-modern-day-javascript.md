# ES6(es 2015)是如何进化并为现代 JavaScript 带来新功能的？

> 原文:[https://www . geesforgeks . org/how-es6-es 2015-进化并为现代带来新功能-javascript/](https://www.geeksforgeeks.org/how-es6-es2015-evolved-and-brought-new-features-to-modern-day-javascript/)

在本文中，我们将在 JavaScript 中看到 ECMAScript 6/ES2015 特性。

**1。Arrow 函数:** Arrow 函数使用= >语法作为其简写。它是传统箭头功能的替代。

让我们来看一个比较传统函数和箭头函数的例子。

## Javascript

```
<script>

    // Without using Arrow Function
    let square = function (x) {
        return (x * x);
    };
    console.log(square(9));

    // Using Arrow Function
    square = (x) => { return x * x; }

    console.log(square(9));

</script>
```