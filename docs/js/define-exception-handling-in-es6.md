# 在 ES6 中定义异常处理

> 原文:[https://www . geesforgeks . org/define-exception-handling-in-es6/](https://www.geeksforgeeks.org/define-exception-handling-in-es6/)

**异常:**异常是基本上中断程序正常流程的不想要的事件。一般有两种例外情况

*   同步(如运行时错误)
*   异步(如系统错误)

**异常处理:**程序中经常发生异常，导致程序突然终止或以不友好的方式终止。处理或防止意外行为被称为异常处理。异常处理处理同步异常，如错误的用户输入、不存在的文件等。(它包括运行时错误)。

**为什么异常处理:**异常处理基本上保证了程序不会突然终止或者程序的流程不会以不友好的方式中断。有意义的错误报告是可能的，并且可以为用户生成可理解的错误报告。

**ES6** (ECMA 脚本编程语言第 6 版)提供了异常处理的重要特性。使用 ***试**—*挡，然后或者 ***抓**—*挡，或者 ***最后**—*挡。由于*尝试*块并不单独存在，所以它们要么后面跟着一个*捕捉*块，要么后面跟着*最终*块。它以三种形式之一存在:-

*   试着…接住
*   尝试…终于
*   尝试…抓住…终于

**1。try…catch block:** Code 或*try*try*block 中的*语句将首先执行。每当异常发生时，它将被置于 *exception_var* 中，并且 *catch* 块将进一步执行。

**语法:**

```
try {

    // try statements 
    // code to run

} catch (exception_var) {

    // catch statements
    // code to run 

}
```

**2。尝试…最后阻止:**首先将执行*尝试*语句。之后*最后执行*语句。*最后*块将总是被执行，不管是否发生异常。

**语法:**

```
try {

    // try statements
    // code to run

} finally {

    // finally statements
    // code that is always executed
}
```

**3。try…catch…finally block:***try*block 首先执行如果发生异常，它的值将被放在 *exception_var* 和 *catch* block 中，然后*最后* block 将被执行。然而，*最后*块将执行，不管异常是否发生。

**语法:**

```
try {

   // try statements
   // code to run

 } catch (exception_var) {

     // catch statements
     // code to run if exception occurs

 } finally {

     // finally statements
     // code that is always executed

 }
```

让我们用下面的例子来理解:

**例 1:** 我们举一个用户输入不好的例子，用户把问题除以零“0”。

## java 描述语言

```
<script>
    var num = 5;
    var de_num = 0;
    try {
        if(de_num == 0) {
            throw "Divide by zero error";
        } else {
            var sol = num / de_num;
        }
    } catch(e) {
        console.log("Error : " + e);
    }
</script>
```

**输出:**

```
Error : Divide by zero error
```

**例 2:** 我们再举一个例子，每当我们使用一个我们没有声明的引用时，就会抛出一个引用错误。在本例中，我们没有有意声明函数，而是直接调用了它，这会导致*引用错误。*

## java 描述语言

```
<script>
    try{
      ab();
      // We have not declared the
      // function ab anywhere
    } catch(e){
      console.log("Error : "+ e.name);
    }
</script>
```

*e.name* 将返回错误的名称。

**输出:**

```
Error : ReferenceError
```

**示例 3:** 在我们的最后一个示例中，我们特意编写了一条语句，试图阻止语法错误。我们没有正确地将字符串括在单引号之间。它会给我们带来*语法错误。*

## java 描述语言

```
<script>
    try {
        eval("alert('ES6 Exception Handling)");
    } catch(e){
        console.log("Error : " + e.name)
    }
</script>
```

**输出**:

```
Error : SyntaxError
```