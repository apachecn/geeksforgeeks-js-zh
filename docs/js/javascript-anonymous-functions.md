# JavaScript 匿名函数

> 原文:[https://www . geesforgeks . org/JavaScript-匿名-函数/](https://www.geeksforgeeks.org/javascript-anonymous-functions/)

**匿名函数**是一个没有任何关联名称的函数。通常我们在函数名前使用*函数*关键字来定义 JavaScript 中的函数，但是在 JavaScript 中的匿名函数中，我们只使用了*函数*关键字而没有函数名。

匿名函数在初始创建后是不可访问的，它只能通过一个变量来访问，该变量作为一个值存储在*函数中。匿名函数也可以有多个参数，但只能有一个表达式。*

**语法:**

```
function() {
    // Function Body
 }
```

下面的例子演示了匿名函数。

**示例 1:** 在本例中，我们定义了一个匿名函数，该函数向控制台打印一条消息。该功能随后存储在*问候*变量中。我们可以通过调用*问候语()来调用该函数。*

## java 描述语言

```
<script>
var greet = function () {
    console.log("Welcome to GeeksforGeeks!");
};

greet();
</script>
```

**输出:**

```
Welcome to GeeksforGeeks!
```

**示例 2:** 在本例中，我们将参数传递给匿名函数。

## java 描述语言

```
<script>
var greet = function (platform) {
    console.log("Welcome to ", platform);
};

greet("GeeksforGeeks!");
</script>
```

**输出:**

```
Welcome to GeeksforGeeks!
```

由于 JavaScript 支持高阶函数，我们也可以将匿名函数作为参数传递给另一个函数。

**示例 3:** 在本例中，我们将一个匿名函数作为回调函数传递给[*setTimeout()*](https://www.geeksforgeeks.org/java-script-settimeout-setinterval-method/)*方法。这将在 2000 毫秒后执行这个匿名函数。*

## *java 描述语言*

```
*<script>
setTimeout(function () {
    console.log("Welcome to GeeksforGeeks!");
}, 2000);
</script>*
```

***输出:***

```
*Welcome to GeeksforGeeks!*
```

*匿名函数的另一个用例是初始化后立即调用函数，这也称为 [*自执行函数*](https://www.geeksforgeeks.org/what-is-the-purpose-of-self-executing-function-in-javascript/) *。*这可以通过添加括号来完成我们可以立即执行匿名函数。*

***示例 4:** 在本例中，我们创建了一个自执行函数。*

## *java 描述语言*

```
*<script>
(function () {
    console.log("Welcome to GeeksforGeeks!");
})();
</script>*
```

***输出:***

```
*Welcome to GeeksforGeeks!*
```

***箭头功能***

*ES6 引入了一种新的更短的匿名函数声明方式，称为 [**箭头函数。**](https://www.geeksforgeeks.org/arrow-functions-in-javascript/) 在一个 Arrow 函数中，一切都保持不变，除了这里我们不需要*函数*关键字也。这里，我们通过单个括号定义函数，然后“= >”后跟函数体。*

***例 5:***

## *java 描述语言*

```
*<script>
var greet = () => 
{
    console.log("Welcome to GeeksforGeeks!");
}

greet();
</script>*
```

***输出:***

```
*Welcome to GeeksforGeeks!*
```

*如果函数体中只有一条语句，我们甚至可以去掉大括号。*

***示例 6:** 在本例中，我们创建了一个自执行函数。*

## *java 描述语言*

```
*<script>
  let greet = () => console.log("Welcome to GeeksforGeeks!");
  greet();
</script>*
```

***输出:***

```
*Welcome to Geeksforgeeks!* 
```