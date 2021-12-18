# JavaScript 库中的前导分号是做什么的？

> 原文:[https://www . geeksforgeeks . org/what-the-leader-in-JavaScript-libraries-do/](https://www.geeksforgeeks.org/what-does-the-leading-semicolon-in-javascript-libraries-do/)

[**JavaScript 中的分号**](https://www.geeksforgeeks.org/javascript-tutorial/) 划分社区。一些开发人员更喜欢一直使用它们。很少有开发者想要避开它们。在某些情况下，省略它们可能会导致不良后果。当两个语句在同一行时，需要分号。所以如果你要把两个语句放在同一行，你必须用分号把它们分开。只有当同一行中有两个或多个语句时，分号才是必需的。应该有一个使用分号来避免错误的良好实践。

**语法:**

```
// Semicolon compulsory
let i = 0; i++  

```

前导分号的**主要目的**是保险的指示，也就是说，如果库嵌入到任何其他代码中，可能是一个有问题的代码，那么它将把最新的语句作为最后一个语句。换句话说，这个分号的目的是**避免一个文件与另一个文件连接时出现错误**。

因为**的问题**是可以解释为之前说法的延续。因此，前导“；”用于 JavaScript 库的前面，以防止当我们在连接过程中将任何文件追加到包含未正确以分号结尾的表达式的文件时出错。JavaScript 分号是可选的&这是可能的，因为 JavaScript 并不严格要求分号，因为它是一个后台进程(自动插入分号)，只要需要就会自动添加。因此，与像 C 语言这样的任何其他语言不同，它并不强制要求在语句末尾使用分号，相反，它在这里是可选的。JavaScript 解释器的工作是在运行任何代码时智能地添加分号。但是如果我们谈论的是连接两个或多个文件，那么为了避免错误，我们必须在 JavaScript 库前面放一个分号。JavaScript 中的一个库显示了一个函数，它以分号
开始**语法:**

```
;(function ){

}

```

**例 1:** 在本例中，我们将不在第一个代码中使用分号，而将在第二个代码中使用。

## java 描述语言

```
let userName = 'Deeksha';

function showMessage() {
  let message = 'hey, ' + userName;
  console.log(message);

}
function ReadMessage() {
  let read = 'You are promoted, ' + userName;
  console.log(read);

}

// When we are concatenating without 
// a semicolon
showMessage()
ReadMessage()
```

**输出:**

```
hey, Deeksha
You are promoted, Deeksha
```

## java 描述语言

```
let userName = 'Deeksha';

function showMessage() {
  let message = 'hey, ' + userName;
  console.log(message);

}
function ReadMessage() {
  let read = 'You are promoted, ' + userName;
  console.log(read);

}

// When we are concatenating with 
// a semicolon
;showMessage();ReadMessage()
```

**输出:**

```
hey, Deeksha
You are promoted, Deeksha
```

**例 2:**

*   **语法:**我们来看一个带有变量的 JavaScript 文件

```
var animal= ”Tiger”

```

*   **语法:**现在，我们来看另一个带有函数的 JavaScript 文件:

```
(function(){})()

```

现在，如果您分别连接这两个文件，效果会很好，但是如果您像通常那样连接它们以减少请求数量，可能会出现错误。

## java 描述语言

```
var animal = "Tiger";

function fun() {
  animal = "Tiger";
  console.log(animal)

}
fun();

var animal = "Tiger";(function(){})()
```

**输出:**

```
Tiger
```

## java 描述语言

```
var animal = "Tiger";

function fun() {
  animal = "Tiger";
  console.log(animal)

}
fun();

var animal = "Tiger"(function(){})()
```

**输出:**

```
Tiger
/home/tim/Personal/Semifinished/index.js:10
var animal = "Tiger"(function(){})()
                    ^

TypeError: "Tiger" is not a function

```

**注意:I** 在上面的过程中，引擎试图调用(First)的结果()但是带有参数 Second。因此，在 JavaScript 库前面添加一个分号来分隔语句以解决这个问题非常重要。