# JavaScript 中的异步/等待功能

> 原文:[https://www . geesforgeks . org/async-wait-function-in-JavaScript/](https://www.geeksforgeeks.org/async-await-function-in-javascript/)

我们都知道，Javascript 是一个同步的，这意味着它有一个事件循环，允许您对一个动作进行排队，直到排队该动作的代码完成执行后循环可用时，该动作才会发生。但是在我们的程序中有很多功能使得我们的代码异步。其中之一是异步/等待功能。

Async/Await 是我们在语言中得到支持的承诺的扩展。你可以参考 Javascript 中的[承诺](https://www.geeksforgeeks.org/javascript-promises/)来了解更多。

**异步:**
它只是允许我们编写基于承诺的代码，就好像它是同步的一样，并且它检查我们没有破坏执行线程。它通过事件循环异步运行。`Async`函数将总是返回值。它确保一个承诺被返回，如果它没有被返回，那么 javascript 自动将它包装在一个承诺中，这个承诺用它的值来解析。

**示例:**

```
const getData = async() => {
    var data = "Hello World";
    return data;
}

getData().then(data => console.log(data));
```

**输出:**

```
Hello World

```

**Await:**
Await 功能用于等待承诺。它只能在异步块中使用。它使代码等待，直到承诺返回结果。它只会让异步块等待。

```
const getData = async() => {
    var y = await "Hello World";
    console.log(y);
}

console.log(1);
getData();
console.log(2);
```

**输出:**

```
1
2
Hello World

```

注意控制台在**“你好世界”**前打印 2。这是因为使用了 await 关键字。

**支持的浏览器:****异步/等待功能**支持的浏览器如下:

*   谷歌 Chrome 55 及以上
*   Firefox 52 及以上版本
*   Apple Safari 10.1 及以上版本
*   歌剧 42 及以上
*   边缘 14 及以上

JavaScript 最出名的是网页开发，但它也用于各种非浏览器环境。您可以通过以下 [JavaScript 教程](https://www.geeksforgeeks.org/javascript-tutorial/)和 [JavaScript 示例](https://www.geeksforgeeks.org/javascript-examples/)从头开始学习 JavaScript。