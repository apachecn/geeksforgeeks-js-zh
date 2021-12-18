# 下划线. js _。()功能后

> 原文:[https://www . geesforgeks . org/下划线-js-_-函数后/](https://www.geeksforgeeks.org/underscore-js-_-after-function/)

**下划线. js** 是一个 JavaScript 库，它提供了许多有用的函数，这些函数在很大程度上有助于编程，比如映射、过滤、调用等，甚至不使用任何内置对象。

**_。after()函数**是 JavaScript 的下划线. js 库中的一个内置函数，用来创建一个函数的包装器，它在开始时什么都不做，但是从所述的*计数*开始调用所述的函数。此外，它在异步响应分组中很有用，因为您需要确定所有异步调用之前是否已经结束。

**语法:**

```
_.after(count, function)
```

**参数:**接受以下指定的两个参数:

*   **计数:**是所述函数被调用后的计数次数。
*   **功能:**是所述的功能。

**返回值:**这个方法返回被调用函数的计数。

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
    </script>
</head>

<body>
    <script>
        show = () => {
            console.log("GeeksforGeeks")
        }
        console.log(`Show function will run for 5 times:`)

        // Calling after function
        func = _.after(3, show);
        func();
        func();
        func();
        func();
        func();
        func();
        func(); 
    </script>
</body>

</html>
```

**输出:**

```
Show function will run for 5 times:
 GeeksforGeeks
 GeeksforGeeks
 GeeksforGeeks
 GeeksforGeeks
 GeeksforGeeks

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
    </script>
</head>

<body>
    <button id="button">button</button>
    <script>
        show = () => {
            console.log("GeeksforGeeks")
        }

        // Calling after function
        func = _.after(3, show);
        let button = document.querySelector("#button");
        let Run = () => {
            console.log(`Show function runs for 8 times:`)
            for (let i = 0; i < 10; i++) {
                func();
            }
        }
        button.addEventListener("click", Run)  
    </script>
</body>

</html>
```

**输出:**

```
button

Show function runs for 7 times:
 GeeksforGeeks
 GeeksforGeeks
 GeeksforGeeks
 GeeksforGeeks
 GeeksforGeeks
 GeeksforGeeks
 GeeksforGeeks
 GeeksforGeeks

```

这里需要点击*按钮*才能看到输出。

**参考:**T2】https://underscorejs.org/#after