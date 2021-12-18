# JavaScript 错误处理:意外令牌

> 原文:[https://www . geesforgeks . org/JavaScript-错误处理-意外-token/](https://www.geeksforgeeks.org/javascript-error-handling-unexpected-token/)

像其他编程语言一样， [**JavaScript**](https://www.geeksforgeeks.org/javascript-tutorial/) 已经定义了一些适当的编程规则。不跟随他们会抛出一个错误。如果 JavaScript 代码缺少或有多余的字符 **{ like，+–var if-else var 等】**，则会出现意外的标记。意外标记类似于语法错误，但更具体。分号(；)在编写程序时，JavaScript 起着至关重要的作用。
**用法:**为了理解这一点，我们应该知道 JavaScript 也有一种特殊的语法，就像在 JavaScript 中是由一个**分号(；)**而且有很多规则像所有**一样空格/制表符/换行符**都被认为是空白。JavaScript 代码是从左到右解析的，这是一个解析器将语句和空白转换成唯一元素的过程。

*   **令牌:**所有的运算符(+、-、if、else…)都被 JavaScript 引擎保留了。所以，不能用错。它不能用作变量名的一部分。
*   **行终止符:**一个 JavaScript 代码应该以分号(；).
*   **控制字符:**要控制代码，在代码中维护大括号({ })很重要。定义代码的范围也很重要。
*   **注释:**写在//之后的一行代码就是注释。JavaScript 忽略了这一行。
*   **空格:**是代码中的制表符/空格。更改它不会更改代码的功能。

因此，JavaScript 代码对任何打字错误都非常敏感。下面给出的这些例子解释了意外令牌可能发生的方式。
**示例 1:** 它要么需要 my unc(my car)中的参数，要么不需要。所以它能够执行这段代码。

## java 描述语言

```
<script>
function multiple(number1, number2) {
    function myFunc(theObject) {
        theObject.make = 'Toyota';
    }
    var mycar = {
        make: 'BMW',
        model: 'Q8-7',
        year: 2005
    };
    var x, y;
    x = mycar.make;
    myFunc(mycar, );
    y = mycar.make;
</script>
```

**输出:**

```
Unexpected end of input
```

**示例 2:** 在 i=0 之后出现了一个 javascript 无法识别的意外标记“，”。我们可以通过移除额外的。

## java 描述语言

```
<script>
for(i=0, ;i<10;i++)
{
  document.writeln(i);
}
</script>
```

**输出:**

```
expected expression, got ', '
```

**示例 3:** 一个意外的 token’)’出现在 i++之后，JavaScript 无法识别。我们可以通过移除额外的来移除错误)。

## java 描述语言

```
<script>
for(i=0;i<10;i++))
{
  console.log(i);
}
</script>
```

**输出**T2】

```
expected expression, got ')'
```

**示例 4:** 在 if 的主体末尾，JavaScript 期望使用大括号“}”，但是它得到了一个意外的标记 else。如果我们把}放在 If 的末尾。

## java 描述语言

```
<script>
var n = 10;
if (n == 10) {
    console.log("TRUE");
    else {
        console.log("FALSE");
    }
</script>
```

**输出**T2】

```
expected expression, got keyword 'else'
```

同样，任何令牌的不必要使用都会引发这种类型的错误。我们可以通过遵循 JavaScript 的编程规则进行绑定来消除这个错误。