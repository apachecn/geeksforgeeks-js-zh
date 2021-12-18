# JavaScript 课程| JavaScript 中的循环

> 原文:[https://www . geesforgeks . org/JavaScript-course-loops-in-JavaScript/](https://www.geeksforgeeks.org/javascript-course-loops-in-javascript/)

**上一个主题:** [JavaScript 课程|练习测验-2](https://www.geeksforgeeks.org/javascript-course-quiz-2/)
在编程语言中循环是一种功能，它有助于在某些条件评估为真时重复执行一组指令/函数。例如，假设我们要打印 10 次“Hello World”。
**例:**

```
<script>
document.write('Hello World'+'<br/>');
document.write('Hello World'+'<br/>');
document.write('Hello World'+'<br/>');
document.write('Hello World'+'<br/>');
document.write('Hello World'+'<br/>');
document.write('Hello World'+'<br/>');
document.write('Hello World'+'<br/>');
document.write('Hello World'+'<br/>');
document.write('Hello World'+'<br/>');
document.write('Hello World'+'<br/>');
</script>
```

上面的代码将简单地向屏幕输出句子“Hello World”10 次。虽然这种方法我不会推荐。虽然有人可能会说你可以写 console.log '10 '次，但是打印一下 console.log '100 '或者说' 10000 '次怎么样。在这些情况下，上述方法并不是任何人都会推荐的，这就是我们使用循环的原因。
Javascript 提供了不同类型的循环。

*   while 循环
*   做..while 循环
*   for 循环

**注:** Javascript 还包括*为..在*、*为..各*、*为..虽然它们超出了本课程的范围。*

**while 循环**
while 循环是一种控制流语句，允许基于给定的布尔条件重复执行代码。while 循环可以看作是一个重复的 if 语句。

```
while(condition){
 do..this;
}

```

我们在 while 循环的括号内传递的条件/表达式必须计算为 true，否则我们在 while 循环的块内编写的语句将不会被执行。
**例:**

```
<script>
// working while loop example
let i = 0;
while( i < 5){
 document.write('Hello World'+'<br/>');
 i++; // necessary to increase the iterator value
} 
</script>
```

**输出:**

```
Hello World
Hello World
Hello World
Hello World
Hello World

```

上面的代码只是将“Hello world”打印到屏幕上，我们所做的就是初始化一个值为“0”的变量“I”，然后我们说，直到这个变量“I”的值小于“10”为止，继续执行 while 循环的块内所写的任何操作。增加变量“I”的值很重要，否则它将进入“无限”循环。现在考虑这样一个场景，我们在圆括号内传递一个值不为真的东西，在这种情况下，代码块内的任何内容都不会被执行。
**例:**

```
<script>
// not working while loop
let i = 5;
while( i < 4 ){
 document.write('Hello World');
 i++;
}
</script>
```

由于 while 循环中的条件没有评估为真，因此屏幕上不会打印任何内容。

**做..while 循环**
do while 循环类似于 while 循环，唯一的区别是它在执行语句后检查条件。不管 while 括号内的条件是否成立，循环至少会运行一次。

```
do
{
    statements..
}
while (condition);

```

**示例:**

```
<script>
// do while loop
// JavaScript program to illustrate do-while loop 
    let x = 21; 

    do 
    { 
        document.write("Value of x: " + x + "<br />"); 
        x++; 
    } while (x < 20); 

</script> 
```

**输出:**

```
Value of x: 21

```

**For 循环**
For 循环提供了一种简洁的编写循环结构的方式。与 while 循环不同，for 语句在一行中消耗初始化、条件和增量/减量，从而提供一个更短、更易于调试的循环结构。

```
for (initialization condition; testing condition;  increment/decrement) {
  do..this;
}

```

*   **初始化条件**:这里我们初始化正在使用的变量。它标志着 for 循环的开始。可以使用已经声明的变量，也可以声明一个变量，只限于局部循环。
*   **测试条件**:用于测试一个回路的退出条件。它必须返回一个布尔值。它也是一个入口控制循环，因为在执行循环语句之前会检查条件。
*   **语句执行**:条件评估为真后，执行循环体中的语句。
*   **递增/递减**:用于更新下一次迭代的变量。
*   **循环终止**:当条件变为假时，循环终止，标志着其生命周期的结束。

**示例:**

```
<script>
// for loop
for(let i = 0; i < 5;i++){
 document.write('Value of i is: ' + i +'<br/>' );
}
</script>
```

**输出:**

```
Value of i is: 0
Value of i is: 1
Value of i is: 2
Value of i is: 3
Value of i is: 4

```

**下一个主题:** [JavaScript 课程| JavaScript 中的函数](https://www.geeksforgeeks.org/javascript-course-functions-in-javascript/)