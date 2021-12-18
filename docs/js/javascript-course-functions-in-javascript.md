# JavaScript 课程| JavaScript 中的函数

> 原文:[https://www . geesforgeks . org/JavaScript-course-functions-in-JavaScript/](https://www.geeksforgeeks.org/javascript-course-functions-in-javascript/)

**前题:** [JavaScript 课程| JavaScript 中的循环](https://www.geeksforgeeks.org/javascript-course-loops-in-javascript/)
Javascript 函数是主要用于执行特定功能的代码块。我们可以通过调用一个函数来执行它任意多次。
要创建函数，我们使用 function()声明，如:

```
// anonymous function
function(){
 // function...body
}

// function with a name
function displayMessage(){
 // function..body
}
```

javascript 中的函数可以是匿名的，也可以是命名的，这完全取决于谁在编写它们。当我们想要调用函数时，我们使用名称，并使用函数返回的值。
**例:**

## java 描述语言

```
<script>
function displayMessage(){
 alert('How you doin'?');
}
// calling the function twice
displayMessage();
displayMessage();
</script>
```

在上面的代码中，我们简单地编写了一个函数，它创建了一个简单的警报弹出窗口，里面有一条简单的消息，我们运行它的方式是调用函数名。

**局部变量**
在函数体内部声明的变量只在函数块内部可用。
**例:**

## java 描述语言

```
<script>
// local variable example
function displayMessage(){
  let message = 'This is the message';
  alert(message);
}
displayMessage();

alert(message); // gives an error
</script>                   
```

在上面的代码中，我们声明了一个名为 displayMessage()的函数，然后在其中声明了一个变量，然后打印了该变量，并且还尝试在函数块之外打印该变量。试图在其声明的块之外使用变量将导致错误。

**外部变量**
外部变量允许我们在功能代码块内部和外部使用它们。
**例:**

## java 描述语言

```
<script>
// Outer variable
let message = 'This is the message';
function displayMessage(){
  alert('Listen '+message);
}

displayMessage();
alert(message);
</script>
```

让我们看另一个例子，在这里我们了解函数如何修改消息。
**例:**

## java 描述语言

```
<script>
// modifying outer variable
let message = 'This is a message';
function displayMessage(){
  message = 'This is the updated message';
  alert('Listen '+message);
}

alert(message);
displayMessage();
alert(message);
</script>
```

在我们调用函数之前，外部变量保持不变，但是在调用函数之后，值会改变，因此即使是最后一个报警函数也会将改变后的值打印到屏幕上。
**传递参数**
我们甚至可以使用参数将任意数据传递给函数。
**例:**

## java 描述语言

```
<script>
// passing data using parameters
function sayHello(from, via){
  alert('You have a message from ' + from + ' via '+ via);
}
sayHello('Mom', 'WhatsApp');
sayHello('Dad', 'Telegram');
</script>
```

在上面我们简单地传递了两个参数，并在主函数中使用了它们。如果不知何故，没有提供一个或所有参数，那么 javascript 使用默认参数。在这种情况下，它基本上打印“未定义”来代替预期的输出。
**例:**

## java 描述语言

```
<script>
// no parameter assigned
function sayHello(from, via){
alert('You have a message from ' + from + ' via '+ via);
}
sayHello('Mom'); // default 2 parameter
</script>
```

我们也可以使用默认参数。我们简单地在参数体中赋值，比如:
**例**

## java 描述语言

```
<script>
// using default parameter
function sayHello(from, via='not mentioned'){
alert('You have a message from ' + from + ' via '+ via);
}
sayHello('Mom');
</script>
```

**返回值**
一个函数可以将一个值返回给调用它的代码。
**例:**

## java 描述语言

```
<script>
// simple function
function sum(a, b) {
  return a + b;
}

let result = sum(5, 10);
alert( result ); // 15
</script>
```

在上面的代码中，我们简单地创建了一个函数，并在函数参数中传递了两个值，然后将该值存储在一个变量结果中，最后向它发出警报。这通常是使用函数最多的场景。
**下一个主题:** [JavaScript 课程| JavaScript 中的对象](https://www.geeksforgeeks.org/javascript-course-objects-in-javascript/)