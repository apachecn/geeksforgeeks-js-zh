# JavaScript 中的 Quines

> Original: [https://www.geeksforgeeks.org/quines-in-javascript/](https://www.geeksforgeeks.org/quines-in-javascript/)

[Quine](https://www.geeksforgeeks.org/quine-a-self-reproducing-program/)是一个不接受任何输入但输出自己代码副本的程序。 与其他语言不同，在 JavaScript/NodeJS 中编写 Quine 非常容易。 使用的方法是 JavaScript 中的任何函数都可以转换为字符串并可以打印。 这允许我们输出如下所示的函数代码：

**示例：**

## JavaScript

```
function quine() { console.log(quine.toString()) }
```

**示例：**上面的函数打印自己的源代码，但它不是可以执行的文件。 **我们将添加一条语句，以便可以调用它。**

## **JavaScript**

```
<script>
  function quine() {console.log(quine.toString() + " quine();")} quine();
</script>;
```

**发帖主题：Re：Колибри0.7.0**

```
"function quine() { window.runnerWindow.proxyConsole.log
(quine.toString()+\" quine();\") } quine();" 
```

****注意：**我们需要在日志语句中添加一些额外的内容来实现我们的目标。 末尾的**`；`**是不需要的。**

**我们可以把它做得更优雅一些。 我们知道，JavaScript 可以通过使用生命周期([立即调用函数表达式](https://www.geeksforgeeks.org/javascript-immediately-invoked-function-expressions-iife/))使函数在定义后立即运行。 我们将把它合并到我们的代码中，如下所示：**

****示例：****

## **JavaScript**

```
<script>
  ( function quine() {console.log("( " + quine.toString() + " )()")} )()
</script>;
```

**发帖主题：Re：Колибри0.7.0**

```
"( function quine() { window.runnerWindow.proxyConsole.log
(\"( \" + quine.toString() + \" )()\") } )()"
```

**请注意，console.log()语句是根据需要进行操作的。 通过将[箭头运算符](https://www.geeksforgeeks.org/arrow-operator-in-es6-of-javascript/)和[格式字符串](https://www.geeksforgeeks.org/javascript-text-formatting/)添加到这个等式中，我们可以进一步使它更漂亮。 这将生成如下所示的代码。**

****示例：****

## **JavaScript**

```
($=_=>`($=${$})()`)()
```

**为了理解代码，我们去掉了格式字符串中的生活和额外的圆括号。 添加间距是为了使其更加清晰。 第一个`**

 **# JavaScript 中的 Quines

is a variable that contains an arrow function. `_` is a random parameter for the arrow function that remains unused. After the arrow, this is our format-string which can be divided into 2 parts, the String, “$=”, and the Variable which is first `

# JavaScript 中的 Quines

itself. 

**示例：**

## JavaScript

```
{content}#xA0;   =    _    =>    `$=${$}`
```

Quine 必须是可执行的，但这并不意味着导致错误的程序不能是 Quine。 下面的示例仍然是 Quine 的一个示例。 该程序在 NodeJS 的帮助下作为.js 文件执行时，会输出自己的源代码。 NodeJS 在第一行返回一个错误，其余代码是错误的样子。

**示例：**

## JavaScript

```
throw 0
^
0
```**