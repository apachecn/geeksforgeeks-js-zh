# JavaScript |语法

> 原文:[https://www.geeksforgeeks.org/javascript-syntax/](https://www.geeksforgeeks.org/javascript-syntax/)

**JavaScript** 是一种轻量级、动态的计算机编程语言。它用于创建客户端动态页面。它是开源的、跨平台的语言。

**基本语法:**

## Javascript

```
<script> 
document.write("Basic Print method in JavaScript"); 
</script> 
```

JavaScript 语法指的是确定如何构造 JavaScript 程序的一组规则:

```
// Variable declaration
var c, d, e;

// Assign value to the variable
c = 5; 

// Computer value of variables
d = c;
e = c/d;
```

**JavaScript 变量:**JavaScript 变量是要存储数据的存储位置的简单名称。JavaScript 中有两种类型的变量，如下所示:

*   **Local variable:** Declare a variable inside a block or function.
*   **Global variable:** Declare a variable outside a function or with a window object.

**例:**

## Javascript

```
<script>

// Declare a variable and initialize it
// Gloabal variable declaration
var Name="Apple";  

// Function definition
function MyFunction() { 

    // Local variable declaration
    var num = 45;   

    // Display the value of Gloabal variable
    document.writeln(Name);

    // Display the value of local variable
    document.writeln("<br>" + num );
} 

// Function call
MyFunction();

</script>
```

**输出:**

```
Apple
45
```

**JavaScript 运算符:** JavaScript 运算符是用于计算值的符号，或者换句话说，我们可以对操作数执行操作。算术运算符(+、-、*、/)用于计算值，赋值运算符(=、+=、%=)用于将值赋给变量。

**例:**

## Javascript

```
<script>

// Variable Declarations
var x, y, sum;

// Assign value to the variables
x = 3;
y = 23;

// Use arithmetic operator to
// add two numbers
sum = x + y;

document.write(sum);

</script>
```

**输出:**

```
26
```

**JavaScript 表达式:**表达式是值、运算符和变量的组合。它用于计算数值。

**示例:**

## java 描述语言

```
<script>

// Variable Declarations
var x, num, sum;

// Assign value to the variables
x = 20;
y = 30

// Expression to divide a number
num = x / 2;

// Expression to add two numbers
sum = x + y;

document.write(num + "<br>" + sum);

</script>
```

**输出:**

```
10
50
```

**JavaScript 关键字:**关键字是 JavaScript 中有特殊含义的保留字。

```
// var is the keyword used to define the variable
var a, b;

// function is the keyword which tells the browser to create a function
function GFG(){};
```

**JavaScript 注释:**注释被 JavaScript 编译器忽略。它增加了代码的可读性。它添加了代码的建议、信息和警告。任何写在双斜线//(单行注释)之后或/*和*/(多行注释)之间的内容都被视为注释，并被 JavaScript 编译器忽略。

**例:**

## Javascript

```
<script>

// Variable Declarations
var x, num, sum;

// Assign value to the variables
x = 20;
y = 30

/* Expression to add two numbers */
sum = x + y;

document.write(sum);

</script>
```

```
50
```

**JavaScript 数据类型:** JavaScript 提供不同的数据类型来保存变量的不同值。JavaScript 是一种动态编程语言，它意味着不需要指定变量的类型。JavaScript 中有两种类型的数据类型。

*   original data type
*   Non-original (reference) data type

```
// It store string data type
var txt = "GeeksforGeeks";

// It store integer data type
var a = 5;
var b = 5;

// It store Boolean data type
(a == b )

// It store array data type
var places= ["GFG", "Computer", "Hello"];

// It store object data
var Student = {firstName:"Johnny", lastName:"Diaz", age:35, mark:"blueEYE"}
```

**JavaScript 函数:** JavaScript 函数是用于执行某些特定操作的代码块。当有东西调用 JavaScript 函数时，它就会被执行。它调用多次，所以函数是可重用的。

**语法:**

```
function functionName( par1, par2, ....., parn ) {  
    // Function code
}  
```

JavaScript 函数可以包含零个或多个参数。

**例:**

## Javascript

```
<script>

// Function definition
function func() { 

    // Declare a variable
    var num = 45;                 

    // Display the result
    document.writeln(num);    
} 

// Function call
func();

</script>
```

**输出:**

```
45
```