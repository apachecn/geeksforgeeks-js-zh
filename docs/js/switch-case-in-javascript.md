# 在 JavaScript 中切换大小写

> 原文:[https://www.geeksforgeeks.org/switch-case-in-javascript/](https://www.geeksforgeeks.org/switch-case-in-javascript/)

我们在上一篇关于 JavaScript 中 [if-else 语句的文章中，已经学习了在 JavaScript 中使用 if-else 语句进行决策。我们在上一篇文章中已经看到，我们可以使用 if-else 语句基于某个特定条件来执行操作。也就是说，如果条件为真，则执行某项任务，否则如果条件为假，则执行其他任务。](https://www.geeksforgeeks.org/else-statement-javascript/)

JavaScript 中的**开关情况**语句也用于决策目的。在某些情况下，使用 switch case 语句比 if-else 语句更方便。考虑这样一种情况，当我们想要测试一个变量的数百个不同值，并且基于这个测试，我们想要执行一些任务。为此目的使用 if-else 语句比 switch case 语句效率更低，而且会使代码看起来很混乱。

switch case 语句是一个多路分支语句。它提供了一种简单的方法，可以根据表达式的值将执行分派到代码的不同部分。

**语法**:

```
switch (expression)
{
    case value1:
        statement1;
        break;
    case value2:
        statement2;
        break;
    .
    .
    case valueN:
        statementN;
        break;
    default:
        statementDefault;
}

```

解释:

*   *表达式*可以是数字或字符串类型。
*   不允许重复*情况*值。
*   *默认的*语句是可选的。如果传递给 switch 的表达式在任何情况下都与值不匹配，那么将执行默认情况下的语句。
*   开关内部使用 *break* 语句来终止一个语句序列。
*   *break* 语句是可选的。如果省略，执行将继续到下一个案例。

**流程图** :
![](img/b3ac657711032acba364c8f60f2531f9.png)

示例:

```
<script type = "text/javascript">

    // JavaScript program to illustrate switch-case
    let i = 9; 

    switch (i)  
    { 
       case 0: 
           console.log("i is zero."); 
           break; 
       case 1: 
           console.log("i is one."); 
           break; 
       case 2: 
           console.log("i is two."); 
           break; 
       default: 
           console.log("i is greater than 2."); 
    }

</script>
```

输出:

```
i is greater than 2.

```