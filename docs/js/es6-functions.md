# ES6 |功能

> 原文:[https://www.geeksforgeeks.org/es6-functions/](https://www.geeksforgeeks.org/es6-functions/)

**ES6 功能**与正常功能相同，但 ES6 有一些不同。函数是一组指令，接受一些输入，执行一些特定的任务并产生输出。函数是一组可以在程序中随时重用的代码。

**语法:**

```
function func-name() { 
   // body 
}

func-name();  // Calling 
```

**函数类型:**ES6 JavaScript 中有几类函数，下面都提到了:

**参数化函数:**该函数与普通函数相同。我们发送一些被调用函数接受的参数，它对这些参数执行一些任务并产生一个输出。

**语法:**

```
function func-name( p1, p2, . . ., p-n) {   
   // body 
}

func-name(1,"Geek", 3); // calling
```

**示例:**

## java 描述语言

```
<script>
function add( p1, p2) {
   var sum = p1 + p2
   console.log("The sum of the values entered " + sum)
}
add(12, 10)
</script>
```

**输出:**

```
The sum of the values entered 22
```

**可返回函数:**向主函数或调用它的函数返回一些值的函数。

**语法:**

```
function func_name() { 
   // statements 
   return value; 
}
var var_name = func_name
```

**示例:**

## java 描述语言

```
<script>
function geeks( ) { 
    // body
    return 'GeeksforGeeks';
}

// calling
var gfg = geeks()
console.log(gfg)
</script>                   
```

**输出:**

```
GeeksforGeeks
```

**函数中的默认参数:**这个概念在 ES6 版本中是全新的。它类似于 C++中的默认函数。我们只是为参数列表中的参数指定一个默认值。如果没有值传递给它或者它是未定义的，那么参数用这些默认值初始化。

**语法:**

```
// p2 and p3 initialized with a default value
function func-name( p1, p2 = 0, p3 = 2) {
   // body 
}

func - name(1); // calling
```

**示例:**

## java 描述语言

```
<script>
// p2 and p3 initialized with a default value
function sum( p1, p2 = 0, p3 = 2) {
   document.write(p1+p2+p3); //1+0+2= 3
}
sum(1);
</script>
```

**输出:**

```
3
```

**函数中的 Rest 参数:**它不限制可以传递给函数的参数数量。也就是说，我们可以用不同的函数调用向同一个函数发送 1、2、3 或更多的参数。参数写在“…”后面，例如“…p”，“…”定义函数调用可能会传递许多参数。

**语法:**

```
function func-name( ...p) // "p" is the parameter
// "..."  define the "Rest parameters"
{
   // body 
}

// calling
func-name(); // 0 argument
func-name(1); // 1 argument
func-name(1,"Geek"); // 2 arguments
func-name(1,"Geek",3); // 3 arguments
```

**示例:**

## java 描述语言

```
<script>
function RestFunc( ...p) // "p" is the parameter
// "..."  define the "Rest parameters"
{
   document.write(p + "<br>");
}

// calling

RestFunc(1); // 1
RestFunc(2,"GFG"); // 2,GFG
RestFunc(3,"GeeK","GFG"); // 3, GeeK, GFG
</script>
```

**输出:**

```
1
2,GFG
3,GeeK,GFG
```

**匿名函数:**匿名函数是在没有任何命名标识符引用的情况下声明的函数。这些函数在运行时动态声明。它可以接受输入并产生输出。它在最初创建后无法访问。

**语法:**

```
var func = function(arguments)
{
    // body
}
```

**示例:**

## java 描述语言

```
<script>
// "func" refer to the function
var func = function() {
    document.write("GeeksforGeeks");
}

// Calling
func();
</script>
```

**输出:**

```
GeeksforGeeks
```

**Lambda 函数或 Arrow 函数:** Lambda 指匿名函数。它是一个没有名称的函数，但通常作为值传递给另一个函数。Lambda 函数有一个箭头符号，这是 lambda 函数区别于其他函数的主要地方。这是在 ES6 版本中引入的。它也被称为箭头函数。它提供了创建匿名函数的简写。它定义使用 **"= > "** 符号。
**语法:**

*   带有一个返回 x + 1 的参数 x 的匿名函数

```
x => x + 1
```

*   与之前相同，但带有功能体

```
x => {return x + 1}
```

*   2 参数箭头函数

```
(x, y) => x + y
```

*   与之前相同，但带有功能体

```
(x, y) => {return x + y}
```

**示例:**

## java 描述语言

```
<script>
//"=>" is use for arrow or lambda expression
var func = () =>
{
   document.write("Arrow function")
}
func()
</script>
```

**输出:**

```
Arrow function
```

**函数提升:**函数提升是一种 JavaScript 机制，函数可以在其声明之前使用。它只出现在函数声明中。它只是提升了函数名，也提升了实际的函数定义。

**语法:**

```
GFG();  // Calling before definition
function GFG() // Define after calling
{
  // body
}
```

**示例:**

## java 描述语言

```
<script>
func();

// Calling before definition-->Hoisting
// "func" is the function
function func() {
    document.write("GeeksforGeeks");
}
</script> 
```

**输出:**

```
GeeksforGeeks
```

**生成器()函数:**生成器函数就像一个正常的函数。但是正常的函数会一直运行，直到它返回或者结束。在生成器函数中，函数运行直到返回或结束。这是通过使用 yield 关键字代替 return 关键字来完成的。当一个生成器函数被调用时，它返回包含整个生成器迭代器的生成器对象，该迭代器使用 next()方法或 for…of 循环进行迭代。yield 语句暂时挂起函数的执行，并将一个值发送回调用方。最主要的是，当我们多次调用一个函数时，该函数的执行会暂停一个值，在下一次调用中，该函数的执行会从暂停的位置重新开始。

**语法:**

```
function* func-name(){
     yield 'GEEK';
     yield 'GFG';
}

// Object creation of generator function
var v = func-name()
document.write.(v.next().value); //"GEEK" 
document.write.(v.next().value); //GFG
```

**示例:**

## java 描述语言

```
<script>

// Generator Function
function * func() {

    // 3 different value
    // generates by 3 different call
    yield 'python';
    yield 'java';
    yield 'C++';    
}

// Calling the Generate Function
var g = func();
document.write(g.next().value+"<br>"); //python
// Paused execution on "python"

document.write(g.next().value+"<br>"); //java
// Paused execution on "java"

document.write(g.next().value); //c++
// Paused execution on "C++"

// "value" is keyword
</script>
```

**输出:**

```
python
java
C++
```

**立即调用函数:**立即调用函数表达式用于避免提升。它允许公众访问方法，即使变量的隐私不是公开的。这些函数不需要任何显式调用来调用。这个函数的声明也不同于普通函数。total 函数在一对第一括号下声明。这个东西告诉编译器立即执行这个块。这也是使用“！”声明的符号。

**语法:**

*   使用第一个括号:

```
(function ()
{ 
    // body 
}) ();
```

*   使用“！”标志

```
!function ()
{ 
    // body 
}();
```

**示例:**这里第二条语句是立即调用函数表达式，它将在被调用函数的第一条语句之后、被调用函数的最后一条语句之前调用，即使最后一条语句在被调用函数之下。

## java 描述语言

```
<script>

// Immediately Invoked Function Expression
function func() {
    document.write("do"+"<br>");

        // This function invoke immediately
        // after executing previous statement
        (function() { document.write("CODE"+"<br>"); })();

    document.write("at GeeksforGeeks");

    // Using "!" keyword
    document.write("<br><br>do"+"<br>");

        // Same thing using "!" symbol
        !function() { document.write("Practice"+"<br>"); } ();

    document.write("at GeeksforGeeks");
}

// Calling
func();
</script>
```

**输出:**

```
do
CODE
at GeeksforGeeks

do
Practice
at GeeksforGeeks
```