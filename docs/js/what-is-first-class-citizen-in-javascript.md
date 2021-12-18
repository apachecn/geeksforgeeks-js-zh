# 什么是 JavaScript 中的一等公民？

> 原文:[https://www . geesforgeks . org/什么是 javascript 中的一等公民/](https://www.geeksforgeeks.org/what-is-first-class-citizen-in-javascript/)

如果任何编程语言都能够将函数视为值，将它们作为参数传递，并从另一个函数返回一个函数，那么据说编程语言具有**一级函数**，在该编程语言中，这些函数被称为**一级公民**。

函数在 JavaScript 中非常重要且强大。JavaScript 具有作为具有一级功能的语言所需要的所有能力或特性，因此功能被视为**一级公民。**让我们看看作为*一等公民的所有能力。*

**1。将函数视为值的能力:**JavaScript 中的函数可以被视为值，即函数可以作为值存储在变量中。

## Javascript

```
<script>
  var greet = function() {
    console.log("Welcome to GeeksforGeeks!");
  }
  greet();
</script>
```

**输出:**

```
Welcome to GeeksforGeeks!
```

在上例中，一个函数存储在变量 *greet* 中，带括号的变量，即 *greet()* 调用函数体，并在控制台中显示输出。**匿名函数**用在该函数作为值的地方。

**2。能够将函数作为参数传递:**JavaScript 中的函数也能够作为参数传递给另一个函数。我们来看一个例子——

## Javascript

```
<script>
function teacher(){
    return "Teacher";
}

function student(){
    return "Student";
}

function greet(user){
    console.log("Welcome", user());    
}

// Prints "Welcome Teacher"
var message = greet(teacher);

// Prints "Welcome Student" 
var message = greet(student);
</script>
```

**输出:**

```
Welcome
Teacher
Welcome
Student
```

在上例中，当我们将函数*中的参数传为*老师*时，它传递函数体*老师()*并返回字符串“老师”，但是当我们将函数*中的参数传为*学生*时，它传递函数体*学生()*并返回字符串“学生”。

**3。从另一个函数返回函数的能力:**现在，让我们看看 JavaScript 中从另一个函数返回函数的示例-

## JavaScript

```
<script>
var greet = function(){
    return function(){
    console.log("Welcome to GeeksforGeeks!");
    }
}
greet()();
</script>
```

**输出:**

```
Welcome to GeeksforGeeks!
```

这里，我们使用**双括号**来调用返回的函数，因此我们使用 *greet()()。*单个括号将调用函数本身，而不调用其返回的函数。我们也可以通过将函数存储在像这样的变量中来实现-

```
var func = greet();
func();
```

返回函数的函数称为 [**【高阶函数】**](https://www.geeksforgeeks.org/higher-order-arrow-functions-in-javascript/) **。**

正如我们所看到的，JavaScript 具有作为一种具有*一级函数*的编程语言所需的所有能力和特性，因此 JavaScript 中的函数被称为*一级公民。*